---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491613"
---
# <span data-ttu-id="796d1-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="796d1-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="796d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="796d1-102">SYNOPSIS</span></span>
<span data-ttu-id="796d1-103">Crea una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="796d1-103">Creates a storage table.</span></span>

## <span data-ttu-id="796d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="796d1-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="796d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="796d1-105">DESCRIPTION</span></span>
<span data-ttu-id="796d1-106">Il cmdlet **New-AzureStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="796d1-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="796d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="796d1-107">EXAMPLES</span></span>

### <span data-ttu-id="796d1-108">Esempio 1: creare una tabella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="796d1-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="796d1-109">Questo comando crea una tabella di archiviazione con il nome tableabc.</span><span class="sxs-lookup"><span data-stu-id="796d1-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="796d1-110">Esempio 2: creare più tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="796d1-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="796d1-111">Questo comando crea più tabelle.</span><span class="sxs-lookup"><span data-stu-id="796d1-111">This command creates multiple tables.</span></span>
<span data-ttu-id="796d1-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="796d1-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="796d1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="796d1-113">PARAMETERS</span></span>

### <span data-ttu-id="796d1-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="796d1-114">-Context</span></span>
<span data-ttu-id="796d1-115">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="796d1-115">Specifies the storage context.</span></span>
<span data-ttu-id="796d1-116">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="796d1-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="796d1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="796d1-117">-Name</span></span>
<span data-ttu-id="796d1-118">Specifica un nome per la nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="796d1-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="796d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796d1-119">CommonParameters</span></span>
<span data-ttu-id="796d1-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796d1-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="796d1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796d1-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="796d1-122">INPUTS</span></span>

## <span data-ttu-id="796d1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="796d1-123">OUTPUTS</span></span>

## <span data-ttu-id="796d1-124">Note</span><span class="sxs-lookup"><span data-stu-id="796d1-124">NOTES</span></span>

## <span data-ttu-id="796d1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="796d1-125">RELATED LINKS</span></span>

[<span data-ttu-id="796d1-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="796d1-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="796d1-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="796d1-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


