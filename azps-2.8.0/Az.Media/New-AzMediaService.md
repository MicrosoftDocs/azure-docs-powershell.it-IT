---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: 77ae2d0713f2b873f40e8335457683dcfbf5eafb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673860"
---
# <span data-ttu-id="159c1-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="159c1-101">New-AzMediaService</span></span>

## <span data-ttu-id="159c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="159c1-102">SYNOPSIS</span></span>
<span data-ttu-id="159c1-103">Crea un servizio multimediale se il servizio multimediale esiste già, tutte le relative proprietà vengono aggiornate con l'input fornito.</span><span class="sxs-lookup"><span data-stu-id="159c1-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="159c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="159c1-104">SYNTAX</span></span>

### <span data-ttu-id="159c1-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="159c1-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="159c1-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="159c1-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="159c1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="159c1-107">DESCRIPTION</span></span>
<span data-ttu-id="159c1-108">Il cmdlet **New-AzMediaService** crea un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="159c1-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="159c1-109">Se il servizio multimediale esiste già, questo cmdlet aggiorna le proprie proprietà.</span><span class="sxs-lookup"><span data-stu-id="159c1-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="159c1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="159c1-110">EXAMPLES</span></span>

### <span data-ttu-id="159c1-111">Esempio1: creare un servizio multimediale solo con l'account di archiviazione principale</span><span class="sxs-lookup"><span data-stu-id="159c1-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="159c1-112">Questo esempio Mostra come creare un servizio multimediale specificando solo l'account di archiviazione principale.</span><span class="sxs-lookup"><span data-stu-id="159c1-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="159c1-113">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="159c1-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="159c1-114">Esempio 2: creare un servizio multimediale con più spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="159c1-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="159c1-115">Questo esempio Mostra come creare un servizio multimediale con più account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="159c1-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="159c1-116">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="159c1-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="159c1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="159c1-117">PARAMETERS</span></span>

### <span data-ttu-id="159c1-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="159c1-118">-AccountName</span></span>
<span data-ttu-id="159c1-119">Specifica il nome del servizio multimediale creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="159c1-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159c1-120">-DefaultProfile</span></span>
<span data-ttu-id="159c1-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="159c1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="159c1-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="159c1-122">-Location</span></span>
<span data-ttu-id="159c1-123">Specifica l'area geografica in cui questo cmdlet crea il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="159c1-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159c1-124">-ResourceGroupName</span></span>
<span data-ttu-id="159c1-125">Specifica il nome del gruppo di risorse a cui è assegnato il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="159c1-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="159c1-126">-StorageAccountId</span></span>
<span data-ttu-id="159c1-127">Specifica l'account di archiviazione associato all'account del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="159c1-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="159c1-128">-StorageAccounts</span></span>
<span data-ttu-id="159c1-129">Specifica una matrice di account di archiviazione da associare al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="159c1-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="159c1-130">-Tag</span></span>
<span data-ttu-id="159c1-131">Tag associati all'account del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="159c1-131">The tags associated with the media service account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="159c1-132">-Confirm</span></span>
<span data-ttu-id="159c1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="159c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="159c1-134">-WhatIf</span></span>
<span data-ttu-id="159c1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="159c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="159c1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="159c1-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159c1-137">CommonParameters</span></span>
<span data-ttu-id="159c1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="159c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159c1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="159c1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159c1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="159c1-140">INPUTS</span></span>

### <span data-ttu-id="159c1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="159c1-141">System.String</span></span>

### <span data-ttu-id="159c1-142">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="159c1-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="159c1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="159c1-143">OUTPUTS</span></span>

### <span data-ttu-id="159c1-144">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="159c1-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="159c1-145">Note</span><span class="sxs-lookup"><span data-stu-id="159c1-145">NOTES</span></span>

## <span data-ttu-id="159c1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="159c1-146">RELATED LINKS</span></span>

[<span data-ttu-id="159c1-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="159c1-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="159c1-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="159c1-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="159c1-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="159c1-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

