---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376274"
---
# <span data-ttu-id="40c5d-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5d-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="40c5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="40c5d-103">Ottiene un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40c5d-103">Gets a Storage account.</span></span>

## <span data-ttu-id="40c5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40c5d-104">SYNTAX</span></span>

### <span data-ttu-id="40c5d-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c5d-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40c5d-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c5d-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40c5d-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c5d-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40c5d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40c5d-108">DESCRIPTION</span></span>
<span data-ttu-id="40c5d-109">Il cmdlet **Get-AzStorageAccount** ottiene un account di archiviazione specificato o tutti gli account di archiviazione in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="40c5d-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="40c5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40c5d-110">EXAMPLES</span></span>

### <span data-ttu-id="40c5d-111">Esempio 1: ottenere un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="40c5d-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="40c5d-112">Questo comando ottiene l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="40c5d-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="40c5d-113">Esempio 2: ottenere tutti gli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="40c5d-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="40c5d-114">Questo comando consente di ottenere tutti gli account di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40c5d-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="40c5d-115">Esempio 3: ottenere tutti gli account di archiviazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="40c5d-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="40c5d-116">Questo comando consente di ottenere tutti gli account di archiviazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="40c5d-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="40c5d-117">Esempio 4: ottenere un account di archiviazione con lo stato di ripristino BLOB</span><span class="sxs-lookup"><span data-stu-id="40c5d-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="40c5d-118">Questo comando ottiene un account di archiviazione con lo stato di ripristino BLOB e Mostra lo stato di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="40c5d-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="40c5d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40c5d-119">PARAMETERS</span></span>

### <span data-ttu-id="40c5d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40c5d-120">-AsJob</span></span>
<span data-ttu-id="40c5d-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="40c5d-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c5d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c5d-122">-DefaultProfile</span></span>
<span data-ttu-id="40c5d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40c5d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c5d-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="40c5d-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="40c5d-125">Ottenere il BlobRestoreStatus dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40c5d-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c5d-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="40c5d-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="40c5d-127">Ottenere il GeoReplicationStats dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40c5d-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c5d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="40c5d-128">-Name</span></span>
<span data-ttu-id="40c5d-129">Specifica il nome dell'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="40c5d-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c5d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c5d-130">-ResourceGroupName</span></span>
<span data-ttu-id="40c5d-131">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="40c5d-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c5d-132">CommonParameters</span></span>
<span data-ttu-id="40c5d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c5d-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c5d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c5d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40c5d-135">INPUTS</span></span>

### <span data-ttu-id="40c5d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="40c5d-136">System.String</span></span>

## <span data-ttu-id="40c5d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40c5d-137">OUTPUTS</span></span>

### <span data-ttu-id="40c5d-138">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="40c5d-139">Note</span><span class="sxs-lookup"><span data-stu-id="40c5d-139">NOTES</span></span>

## <span data-ttu-id="40c5d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40c5d-140">RELATED LINKS</span></span>

[<span data-ttu-id="40c5d-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5d-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="40c5d-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5d-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="40c5d-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5d-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


