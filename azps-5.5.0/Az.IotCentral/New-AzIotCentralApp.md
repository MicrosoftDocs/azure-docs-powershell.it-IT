---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187647"
---
# <span data-ttu-id="acd9b-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="acd9b-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="acd9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd9b-102">SYNOPSIS</span></span>
<span data-ttu-id="acd9b-103">Crea una nuova applicazione IoT Central.</span><span class="sxs-lookup"><span data-stu-id="acd9b-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="acd9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acd9b-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acd9b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="acd9b-105">DESCRIPTION</span></span>
<span data-ttu-id="acd9b-106">Crea una nuova applicazione IoT Central con le proprietà e i metadati forniti.</span><span class="sxs-lookup"><span data-stu-id="acd9b-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="acd9b-107">Per un'introduzione a IoT Central, vedere https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="acd9b-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="acd9b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acd9b-108">EXAMPLES</span></span>

### <span data-ttu-id="acd9b-109">Esempio 1: Creare una semplice applicazione centrale IoT.</span><span class="sxs-lookup"><span data-stu-id="acd9b-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="acd9b-110">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="acd9b-110">Example Output:</span></span>

<span data-ttu-id="acd9b-111">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Sottodominio MyAppResourceName : Modello MyAppSubdomain iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd9b-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="acd9b-112">Creare un'applicazione IoT Central nel piano prezzi standard ST2, nell'area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="acd9b-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="acd9b-113">Esempio 2: Creare una semplice applicazione centrale IoT.</span><span class="sxs-lookup"><span data-stu-id="acd9b-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="acd9b-114">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="acd9b-114">Example Output:</span></span>

<span data-ttu-id="acd9b-115">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd9b-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="acd9b-116">Creare un'applicazione IoT Central con il piano di prezzi standard ST2 nell'area "ovest", con un nome visualizzato personalizzato basato sul modello iotc-default.</span><span class="sxs-lookup"><span data-stu-id="acd9b-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="acd9b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd9b-117">PARAMETERS</span></span>

### <span data-ttu-id="acd9b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acd9b-118">-AsJob</span></span>
<span data-ttu-id="acd9b-119">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="acd9b-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="acd9b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd9b-120">-DefaultProfile</span></span>
<span data-ttu-id="acd9b-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acd9b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd9b-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="acd9b-122">-DisplayName</span></span>
<span data-ttu-id="acd9b-123">Nome visualizzato personalizzato per l'applicazione IoT Central.</span><span class="sxs-lookup"><span data-stu-id="acd9b-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="acd9b-124">L'impostazione predefinita è il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="acd9b-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-125">-Location</span><span class="sxs-lookup"><span data-stu-id="acd9b-125">-Location</span></span>
<span data-ttu-id="acd9b-126">Posizione dell'applicazione IoT Central.</span><span class="sxs-lookup"><span data-stu-id="acd9b-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="acd9b-127">L'impostazione predefinita è la posizione del gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acd9b-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="acd9b-128">-Name</span></span>
<span data-ttu-id="acd9b-129">Nome della risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="acd9b-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd9b-130">-ResourceGroupName</span></span>
<span data-ttu-id="acd9b-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="acd9b-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="acd9b-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="acd9b-132">-Sku</span></span>
<span data-ttu-id="acd9b-133">Pricing tier per le applicazioni IoT Central.</span><span class="sxs-lookup"><span data-stu-id="acd9b-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="acd9b-134">Il valore predefinito è ST2.</span><span class="sxs-lookup"><span data-stu-id="acd9b-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="acd9b-135">-Subdomain</span></span>
<span data-ttu-id="acd9b-136">Sottodominio per l'URL centrale IoT.</span><span class="sxs-lookup"><span data-stu-id="acd9b-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="acd9b-137">Ogni applicazione deve avere un sottodominio univoco.</span><span class="sxs-lookup"><span data-stu-id="acd9b-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="acd9b-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="acd9b-138">-Tag</span></span>
<span data-ttu-id="acd9b-139">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="acd9b-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-140">-Template</span><span class="sxs-lookup"><span data-stu-id="acd9b-140">-Template</span></span>
<span data-ttu-id="acd9b-141">Nome del modello di applicazione IoT Central.</span><span class="sxs-lookup"><span data-stu-id="acd9b-141">IoT Central application template name.</span></span>
<span data-ttu-id="acd9b-142">L'impostazione predefinita è un'applicazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="acd9b-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acd9b-143">-Confirm</span></span>
<span data-ttu-id="acd9b-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acd9b-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd9b-145">-WhatIf</span></span>
<span data-ttu-id="acd9b-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acd9b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd9b-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acd9b-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd9b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd9b-148">CommonParameters</span></span>
<span data-ttu-id="acd9b-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd9b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd9b-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acd9b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd9b-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="acd9b-151">INPUTS</span></span>

### <span data-ttu-id="acd9b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="acd9b-152">System.String</span></span>

### <span data-ttu-id="acd9b-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="acd9b-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acd9b-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acd9b-154">OUTPUTS</span></span>

### <span data-ttu-id="acd9b-155">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="acd9b-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="acd9b-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="acd9b-156">NOTES</span></span>

## <span data-ttu-id="acd9b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acd9b-157">RELATED LINKS</span></span>
