---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969613"
---
# <span data-ttu-id="fc3c3-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fc3c3-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="fc3c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3c3-103">Creare un oggetto in memoria per l'estensione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="fc3c3-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="fc3c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc3c3-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="fc3c3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc3c3-105">DESCRIPTION</span></span>
<span data-ttu-id="fc3c3-106">Creare un oggetto in memoria per l'estensione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="fc3c3-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="fc3c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc3c3-107">EXAMPLES</span></span>

### <span data-ttu-id="fc3c3-108">Esempio 1: Creare un oggetto estensione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="fc3c3-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="fc3c3-109">Questo comando crea un oggetto estensione di diagnostica usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="fc3c3-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="fc3c3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc3c3-111">PARAMETERS</span></span>

### <span data-ttu-id="fc3c3-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fc3c3-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fc3c3-113">Aggiornamento automatico della versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="fc3c3-114">-CloudServiceName</span></span>
<span data-ttu-id="fc3c3-115">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="fc3c3-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="fc3c3-117">Specifica la configurazione per Diagnostica di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="fc3c3-118">È possibile scaricare lo schema usando il comando seguente: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderExtension 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="fc3c3-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fc3c3-119">-Name</span></span>
<span data-ttu-id="fc3c3-120">Nome dell'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-120">Name of Diagnostics Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc3c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc3c3-122">Nome del gruppo di risorse del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-122">Resource Group name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="fc3c3-123">-RolesAppliedTo</span></span>
<span data-ttu-id="fc3c3-124">Ruoli applicati a.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fc3c3-125">-StorageAccountKey</span></span>
<span data-ttu-id="fc3c3-126">Chiave account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fc3c3-127">-StorageAccountName</span></span>
<span data-ttu-id="fc3c3-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-129">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="fc3c3-129">-Subscription</span></span>
<span data-ttu-id="fc3c3-130">Abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fc3c3-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="fc3c3-132">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3c3-133">CommonParameters</span></span>
<span data-ttu-id="fc3c3-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3c3-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc3c3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3c3-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc3c3-136">INPUTS</span></span>

## <span data-ttu-id="fc3c3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc3c3-137">OUTPUTS</span></span>

### <span data-ttu-id="fc3c3-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="fc3c3-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="fc3c3-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc3c3-139">NOTES</span></span>

<span data-ttu-id="fc3c3-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fc3c3-140">ALIASES</span></span>

## <span data-ttu-id="fc3c3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc3c3-141">RELATED LINKS</span></span>

