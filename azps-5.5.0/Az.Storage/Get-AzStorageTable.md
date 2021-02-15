---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195791"
---
# <span data-ttu-id="b6bc6-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="b6bc6-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="b6bc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bc6-103">Elenca le tabelle di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-103">Lists the storage tables.</span></span>

## <span data-ttu-id="b6bc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6bc6-104">SYNTAX</span></span>

### <span data-ttu-id="b6bc6-105">TableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6bc6-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6bc6-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="b6bc6-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6bc6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6bc6-107">DESCRIPTION</span></span>
<span data-ttu-id="b6bc6-108">Il **cmdlet Get-AzStorageTable elenca** le tabelle di archiviazione associate all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="b6bc6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6bc6-109">EXAMPLES</span></span>

### <span data-ttu-id="b6bc6-110">Esempio 1: Elencare tutte le tabelle di Archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="b6bc6-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="b6bc6-111">Questo comando recupera tutte le tabelle di archiviazione per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="b6bc6-112">Esempio 2: Elencare le tabelle di Archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="b6bc6-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="b6bc6-113">Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con tabella.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="b6bc6-114">Esempio 3: Elencare le tabelle di Archiviazione di Azure usando il prefisso del nome della tabella</span><span class="sxs-lookup"><span data-stu-id="b6bc6-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="b6bc6-115">Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con table.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="b6bc6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6bc6-116">PARAMETERS</span></span>

### <span data-ttu-id="b6bc6-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b6bc6-117">-Context</span></span>
<span data-ttu-id="b6bc6-118">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-118">Specifies the storage context.</span></span>
<span data-ttu-id="b6bc6-119">Per crearla, è possibile usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b6bc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bc6-120">-DefaultProfile</span></span>
<span data-ttu-id="b6bc6-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6bc6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b6bc6-122">-Name</span></span>
<span data-ttu-id="b6bc6-123">Specifica il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-123">Specifies the table name.</span></span>
<span data-ttu-id="b6bc6-124">Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="b6bc6-125">In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al criterio del nome normale.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bc6-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b6bc6-126">-Prefix</span></span>
<span data-ttu-id="b6bc6-127">Specifica un prefisso usato nel nome della tabella o delle tabelle da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="b6bc6-128">È possibile usarla per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bc6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bc6-129">CommonParameters</span></span>
<span data-ttu-id="b6bc6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bc6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bc6-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6bc6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bc6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6bc6-132">INPUTS</span></span>

### <span data-ttu-id="b6bc6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b6bc6-133">System.String</span></span>

### <span data-ttu-id="b6bc6-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6bc6-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b6bc6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6bc6-135">OUTPUTS</span></span>

### <span data-ttu-id="b6bc6-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b6bc6-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="b6bc6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6bc6-137">NOTES</span></span>

## <span data-ttu-id="b6bc6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6bc6-138">RELATED LINKS</span></span>

[<span data-ttu-id="b6bc6-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="b6bc6-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="b6bc6-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="b6bc6-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


