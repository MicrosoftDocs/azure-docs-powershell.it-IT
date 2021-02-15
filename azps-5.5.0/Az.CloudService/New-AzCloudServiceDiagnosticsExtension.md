---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: 96651a495f08657a4cd9006545cfa104285ec7ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200742"
---
# <span data-ttu-id="db42f-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db42f-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="db42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db42f-102">SYNOPSIS</span></span>
<span data-ttu-id="db42f-103">Creare un oggetto in memoria per l'estensione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="db42f-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="db42f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db42f-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="db42f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db42f-105">DESCRIPTION</span></span>
<span data-ttu-id="db42f-106">Creare un oggetto in memoria per l'estensione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="db42f-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="db42f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db42f-107">EXAMPLES</span></span>

### <span data-ttu-id="db42f-108">Esempio 1: Creare un oggetto estensione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="db42f-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="db42f-109">Questo comando crea un oggetto estensione di diagnostica usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="db42f-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="db42f-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="db42f-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="db42f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db42f-111">PARAMETERS</span></span>

### <span data-ttu-id="db42f-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="db42f-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="db42f-113">Aggiornamento automatico della versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="db42f-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="db42f-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="db42f-114">-CloudServiceName</span></span>
<span data-ttu-id="db42f-115">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="db42f-115">Name of Cloud Service.</span></span>

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

### <span data-ttu-id="db42f-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="db42f-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="db42f-117">Specifica la configurazione per Diagnostica di Azure.</span><span class="sxs-lookup"><span data-stu-id="db42f-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="db42f-118">È possibile scaricare lo schema usando il comando seguente: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderExtension 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="db42f-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

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

### <span data-ttu-id="db42f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="db42f-119">-Name</span></span>
<span data-ttu-id="db42f-120">Nome dell'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="db42f-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="db42f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db42f-121">-ResourceGroupName</span></span>
<span data-ttu-id="db42f-122">Nome del gruppo di risorse del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="db42f-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="db42f-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="db42f-123">-RolesAppliedTo</span></span>
<span data-ttu-id="db42f-124">Ruoli applicati a.</span><span class="sxs-lookup"><span data-stu-id="db42f-124">Roles applied to.</span></span>

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

### <span data-ttu-id="db42f-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="db42f-125">-StorageAccountKey</span></span>
<span data-ttu-id="db42f-126">Chiave account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db42f-126">Storage Account Key.</span></span>

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

### <span data-ttu-id="db42f-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db42f-127">-StorageAccountName</span></span>
<span data-ttu-id="db42f-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db42f-128">Name of the Storage Account.</span></span>

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

### <span data-ttu-id="db42f-129">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="db42f-129">-Subscription</span></span>
<span data-ttu-id="db42f-130">Abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db42f-130">Subscription.</span></span>

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

### <span data-ttu-id="db42f-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="db42f-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="db42f-132">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="db42f-132">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="db42f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db42f-133">CommonParameters</span></span>
<span data-ttu-id="db42f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db42f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db42f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db42f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db42f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="db42f-136">INPUTS</span></span>

## <span data-ttu-id="db42f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db42f-137">OUTPUTS</span></span>

### <span data-ttu-id="db42f-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="db42f-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="db42f-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="db42f-139">NOTES</span></span>

<span data-ttu-id="db42f-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="db42f-140">ALIASES</span></span>

## <span data-ttu-id="db42f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db42f-141">RELATED LINKS</span></span>

