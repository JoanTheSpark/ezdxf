Blocks Section
==============

The :class:`BlocksSection` class manages all block definitions of a drawing
document.

.. class:: BlocksSection

.. method:: BlocksSection.__iter__()

Iterate over all block definitions, yielding :class:`BlockLayout` objects.

.. method:: BlocksSection.__contains__(entity)

Test if :class:`BlocksSection` contains the block definition `entity`, `entity`
can be a block name as `str` or the :class:`Block` definition itself.

.. method:: BlocksSection.__getitem__(name)

Get the :class:`Block` definition by `name`, raises `KeyError` if no block
`name` exists.

.. method:: BlocksSection.get(name, default=None)

Get the :class:`Block` definition by `name`, returns `default` if no block
`name` exists.

.. method:: BlocksSection.new(name, base_point=(0, 0), dxfattribs=None)

Create and add a new :class:`Block`, `name` is the block-name, `base_point`
is the insertion point of the block.

.. method:: BlocksSection.new_anonymous_block(type_char='U', base_point=(0, 0))

Create and add a new anonymous :class:`Block`, `type_char` is the block-type,
`base_point` is the insertion point of the block.

.. method:: BlocksSection.rename_block(old_name, new_name)

Rename block 'old_name' in 'new_name'.

.. method:: BlockSection.delete_block(name):

Delete block *name*. Raises *KeyError* if block not exists.

.. method:: BlockSection.delete_all_blocks():

========= ==========
type_char Anonymous Block Type
========= ==========
U         \*U### anonymous blocks
E         \*E### anonymous non-uniformly scaled blocks
X         \*X### anonymous hatches
D         \*D### anonymous dimensions
A         \*A### anonymous groups
========= ==========

