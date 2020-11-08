---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191531"
---
# <span data-ttu-id="24f11-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="24f11-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="24f11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24f11-102">SYNOPSIS</span></span>
<span data-ttu-id="24f11-103">Crea una nuova applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="24f11-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="24f11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24f11-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24f11-105">DESCRIPTION</span></span>
<span data-ttu-id="24f11-106">Crea una nuova applicazione centrale di un sacco con le proprietà e i metadati forniti.</span><span class="sxs-lookup"><span data-stu-id="24f11-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="24f11-107">Per un'introduzione al centro informazioni, vedere https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="24f11-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="24f11-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24f11-108">EXAMPLES</span></span>

### <span data-ttu-id="24f11-109">L'esempio 1 crea un'applicazione centrale semplice.</span><span class="sxs-lookup"><span data-stu-id="24f11-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="24f11-110">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="24f11-110">Example Output:</span></span>

<span data-ttu-id="24f11-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx</span><span class="sxs-lookup"><span data-stu-id="24f11-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="24f11-112">Creare un'applicazione centrale molto in ST2 livello prezzi standard nell'area del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="24f11-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="24f11-113">Esempio 2 creare un'applicazione centrale semplice.</span><span class="sxs-lookup"><span data-stu-id="24f11-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="24f11-114">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="24f11-114">Example Output:</span></span>

<span data-ttu-id="24f11-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName nome: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f11-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="24f11-116">Creare un'applicazione centrale molto con il livello di prezzo standard ST2 nell'area "westus", con un nome visualizzato personalizzato, basato sul modello predefinito di IOTC.</span><span class="sxs-lookup"><span data-stu-id="24f11-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="24f11-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24f11-117">PARAMETERS</span></span>

### <span data-ttu-id="24f11-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f11-118">-AsJob</span></span>
<span data-ttu-id="24f11-119">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="24f11-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="24f11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f11-120">-DefaultProfile</span></span>
<span data-ttu-id="24f11-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24f11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f11-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="24f11-122">-DisplayName</span></span>
<span data-ttu-id="24f11-123">Nome visualizzato personalizzato per l'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="24f11-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="24f11-124">L'impostazione predefinita è nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="24f11-124">Default is resource name.</span></span>

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

### <span data-ttu-id="24f11-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24f11-125">-Location</span></span>
<span data-ttu-id="24f11-126">Posizione dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="24f11-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="24f11-127">Il valore predefinito è la posizione del gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="24f11-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="24f11-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="24f11-128">-Name</span></span>
<span data-ttu-id="24f11-129">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="24f11-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="24f11-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f11-130">-ResourceGroupName</span></span>
<span data-ttu-id="24f11-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24f11-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="24f11-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="24f11-132">-Sku</span></span>
<span data-ttu-id="24f11-133">Livello dei prezzi per le applicazioni centrali di un sacco.</span><span class="sxs-lookup"><span data-stu-id="24f11-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="24f11-134">Il valore predefinito è ST2.</span><span class="sxs-lookup"><span data-stu-id="24f11-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="24f11-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="24f11-135">-Subdomain</span></span>
<span data-ttu-id="24f11-136">Sottodominio per l'URL centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="24f11-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="24f11-137">Ogni applicazione deve avere un sottodominio univoco.</span><span class="sxs-lookup"><span data-stu-id="24f11-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="24f11-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="24f11-138">-Tag</span></span>
<span data-ttu-id="24f11-139">Tag delle risorse dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="24f11-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="24f11-140">-Modello</span><span class="sxs-lookup"><span data-stu-id="24f11-140">-Template</span></span>
<span data-ttu-id="24f11-141">Nome del modello di applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="24f11-141">IoT Central application template name.</span></span>
<span data-ttu-id="24f11-142">L'impostazione predefinita è un'applicazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="24f11-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="24f11-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24f11-143">-Confirm</span></span>
<span data-ttu-id="24f11-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f11-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f11-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f11-145">-WhatIf</span></span>
<span data-ttu-id="24f11-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24f11-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f11-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24f11-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f11-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f11-148">CommonParameters</span></span>
<span data-ttu-id="24f11-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f11-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f11-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24f11-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f11-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24f11-151">INPUTS</span></span>

### <span data-ttu-id="24f11-152">System. String</span><span class="sxs-lookup"><span data-stu-id="24f11-152">System.String</span></span>

### <span data-ttu-id="24f11-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24f11-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24f11-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24f11-154">OUTPUTS</span></span>

### <span data-ttu-id="24f11-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="24f11-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="24f11-156">Note</span><span class="sxs-lookup"><span data-stu-id="24f11-156">NOTES</span></span>

## <span data-ttu-id="24f11-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24f11-157">RELATED LINKS</span></span>
