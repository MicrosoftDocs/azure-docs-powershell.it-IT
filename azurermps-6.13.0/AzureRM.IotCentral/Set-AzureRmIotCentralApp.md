---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688416"
---
# <span data-ttu-id="7460c-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7460c-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="7460c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7460c-102">SYNOPSIS</span></span>
<span data-ttu-id="7460c-103">Aggiorna i metadati per un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7460c-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7460c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7460c-104">SYNTAX</span></span>

### <span data-ttu-id="7460c-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7460c-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7460c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7460c-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7460c-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="7460c-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7460c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7460c-108">DESCRIPTION</span></span>
<span data-ttu-id="7460c-109">Aggiornare i metadati per un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7460c-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="7460c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7460c-110">EXAMPLES</span></span>

### <span data-ttu-id="7460c-111">Esempio 1 Aggiorna nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="7460c-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="7460c-112">Aggiornare il nome visualizzato in un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="7460c-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7460c-113">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="7460c-113">Example Output:</span></span>

<span data-ttu-id="7460c-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName nome: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom nome visualizzato subdomain: MyAppSubdomain Template: SubscriptionID iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7460c-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="7460c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7460c-115">PARAMETERS</span></span>

### <span data-ttu-id="7460c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7460c-116">-AsJob</span></span>
<span data-ttu-id="7460c-117">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="7460c-117">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7460c-118">-DefaultProfile</span></span>
<span data-ttu-id="7460c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7460c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7460c-120">-DisplayName</span></span>
<span data-ttu-id="7460c-121">Nome visualizzato personalizzato dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7460c-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7460c-122">-InputObject</span></span>
<span data-ttu-id="7460c-123">Oggetto di input dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="7460c-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7460c-124">-Name</span></span>
<span data-ttu-id="7460c-125">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7460c-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7460c-126">-ResourceGroupName</span></span>
<span data-ttu-id="7460c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7460c-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7460c-128">-ResourceId</span></span>
<span data-ttu-id="7460c-129">ID risorsa centrale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7460c-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7460c-130">-Tag</span></span>
<span data-ttu-id="7460c-131">Tag delle risorse dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="7460c-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7460c-132">-Confirm</span></span>
<span data-ttu-id="7460c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7460c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7460c-134">-WhatIf</span></span>
<span data-ttu-id="7460c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7460c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7460c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7460c-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7460c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7460c-137">CommonParameters</span></span>
<span data-ttu-id="7460c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7460c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7460c-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7460c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7460c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7460c-140">INPUTS</span></span>

### <span data-ttu-id="7460c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7460c-141">System.String</span></span>
### <span data-ttu-id="7460c-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7460c-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="7460c-143">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7460c-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="7460c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7460c-144">OUTPUTS</span></span>

### <span data-ttu-id="7460c-145">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7460c-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="7460c-146">Note</span><span class="sxs-lookup"><span data-stu-id="7460c-146">NOTES</span></span>

## <span data-ttu-id="7460c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7460c-147">RELATED LINKS</span></span>
