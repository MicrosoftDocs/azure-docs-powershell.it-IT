---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348136"
---
# <span data-ttu-id="189ed-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="189ed-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="189ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="189ed-102">SYNOPSIS</span></span>
<span data-ttu-id="189ed-103">Aggiorna i metadati per un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="189ed-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="189ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="189ed-104">SYNTAX</span></span>

### <span data-ttu-id="189ed-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="189ed-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189ed-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="189ed-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189ed-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="189ed-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="189ed-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="189ed-108">DESCRIPTION</span></span>
<span data-ttu-id="189ed-109">Aggiornare i metadati per un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="189ed-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="189ed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="189ed-110">EXAMPLES</span></span>

### <span data-ttu-id="189ed-111">Esempio 1 Aggiorna nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="189ed-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="189ed-112">Aggiornare il nome visualizzato in un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="189ed-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="189ed-113">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="189ed-113">Example Output:</span></span>

<span data-ttu-id="189ed-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName nome: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom nome visualizzato subdomain: MyAppSubdomain Template: SubscriptionID iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189ed-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="189ed-115">Esempio 2 aggiornamento del sottodominio</span><span class="sxs-lookup"><span data-stu-id="189ed-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="189ed-116">Aggiornare il nome visualizzato in un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="189ed-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="189ed-117">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="189ed-117">Example Output:</span></span>

<span data-ttu-id="189ed-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: display subdomain Name: New-subdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189ed-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="189ed-119">Esempio 3 informazioni SKU dell'app di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="189ed-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="189ed-120">Aggiornare l'USK in un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="189ed-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="189ed-121">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="189ed-121">Example Output:</span></span>

<span data-ttu-id="189ed-122">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: display subdomain Name: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189ed-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="189ed-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="189ed-123">PARAMETERS</span></span>

### <span data-ttu-id="189ed-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="189ed-124">-AsJob</span></span>
<span data-ttu-id="189ed-125">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="189ed-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="189ed-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189ed-126">-DefaultProfile</span></span>
<span data-ttu-id="189ed-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="189ed-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="189ed-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="189ed-128">-DisplayName</span></span>
<span data-ttu-id="189ed-129">Nome visualizzato personalizzato dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="189ed-129">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189ed-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="189ed-130">-InputObject</span></span>
<span data-ttu-id="189ed-131">Oggetto di input dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="189ed-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="189ed-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="189ed-132">-Name</span></span>
<span data-ttu-id="189ed-133">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="189ed-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189ed-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189ed-134">-ResourceGroupName</span></span>
<span data-ttu-id="189ed-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="189ed-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189ed-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="189ed-136">-ResourceId</span></span>
<span data-ttu-id="189ed-137">ID risorsa centrale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="189ed-137">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="189ed-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="189ed-138">-Sku</span></span>
<span data-ttu-id="189ed-139">Livello dei prezzi per le applicazioni centrali di un sacco.</span><span class="sxs-lookup"><span data-stu-id="189ed-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="189ed-140">Il valore predefinito è ST2.</span><span class="sxs-lookup"><span data-stu-id="189ed-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="189ed-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="189ed-141">-Subdomain</span></span>
<span data-ttu-id="189ed-142">Sottodominio dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="189ed-142">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189ed-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="189ed-143">-Tag</span></span>
<span data-ttu-id="189ed-144">Tag delle risorse dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="189ed-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="189ed-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="189ed-145">-Confirm</span></span>
<span data-ttu-id="189ed-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="189ed-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189ed-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189ed-147">-WhatIf</span></span>
<span data-ttu-id="189ed-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="189ed-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189ed-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="189ed-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189ed-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189ed-150">CommonParameters</span></span>
<span data-ttu-id="189ed-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="189ed-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189ed-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="189ed-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189ed-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="189ed-153">INPUTS</span></span>

### <span data-ttu-id="189ed-154">System. String</span><span class="sxs-lookup"><span data-stu-id="189ed-154">System.String</span></span>

### <span data-ttu-id="189ed-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="189ed-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="189ed-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="189ed-156">OUTPUTS</span></span>

### <span data-ttu-id="189ed-157">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="189ed-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="189ed-158">Note</span><span class="sxs-lookup"><span data-stu-id="189ed-158">NOTES</span></span>

## <span data-ttu-id="189ed-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="189ed-159">RELATED LINKS</span></span>
