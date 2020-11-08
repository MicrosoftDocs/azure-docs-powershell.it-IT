---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022642"
---
# <span data-ttu-id="22fc1-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="22fc1-101">New-AzStorageTable</span></span>

## <span data-ttu-id="22fc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="22fc1-103">Crea una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="22fc1-103">Creates a storage table.</span></span>

## <span data-ttu-id="22fc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22fc1-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22fc1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="22fc1-106">Il cmdlet **New-AzStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="22fc1-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="22fc1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22fc1-107">EXAMPLES</span></span>

### <span data-ttu-id="22fc1-108">Esempio 1: creare una tabella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="22fc1-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="22fc1-109">Questo comando crea una tabella di archiviazione con il nome tableabc.</span><span class="sxs-lookup"><span data-stu-id="22fc1-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="22fc1-110">Esempio 2: creare più tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="22fc1-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="22fc1-111">Questo comando crea più tabelle.</span><span class="sxs-lookup"><span data-stu-id="22fc1-111">This command creates multiple tables.</span></span>
<span data-ttu-id="22fc1-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="22fc1-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="22fc1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22fc1-113">PARAMETERS</span></span>

### <span data-ttu-id="22fc1-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="22fc1-114">-Context</span></span>
<span data-ttu-id="22fc1-115">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="22fc1-115">Specifies the storage context.</span></span>
<span data-ttu-id="22fc1-116">Per crearlo, puoi usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="22fc1-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22fc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22fc1-117">-DefaultProfile</span></span>
<span data-ttu-id="22fc1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22fc1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22fc1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="22fc1-119">-Name</span></span>
<span data-ttu-id="22fc1-120">Specifica un nome per la nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="22fc1-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22fc1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22fc1-121">CommonParameters</span></span>
<span data-ttu-id="22fc1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22fc1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22fc1-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22fc1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22fc1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22fc1-124">INPUTS</span></span>

### <span data-ttu-id="22fc1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="22fc1-125">System.String</span></span>

### <span data-ttu-id="22fc1-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="22fc1-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="22fc1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22fc1-127">OUTPUTS</span></span>

### <span data-ttu-id="22fc1-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="22fc1-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="22fc1-129">Note</span><span class="sxs-lookup"><span data-stu-id="22fc1-129">NOTES</span></span>

## <span data-ttu-id="22fc1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22fc1-130">RELATED LINKS</span></span>

[<span data-ttu-id="22fc1-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="22fc1-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="22fc1-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="22fc1-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


