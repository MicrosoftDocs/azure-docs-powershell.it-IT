---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334519"
---
# <span data-ttu-id="1afa6-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="1afa6-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="1afa6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1afa6-102">SYNOPSIS</span></span>
<span data-ttu-id="1afa6-103">Genera un token SAS per un hub, un dispositivo o un modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1afa6-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="1afa6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1afa6-104">SYNTAX</span></span>

### <span data-ttu-id="1afa6-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1afa6-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afa6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1afa6-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1afa6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1afa6-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1afa6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1afa6-108">DESCRIPTION</span></span>
<span data-ttu-id="1afa6-109">Per i token SAS per i dispositivi, il parametro policy viene usato per accedere solo al registro di sistema del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1afa6-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="1afa6-110">Di conseguenza, il criterio dovrebbe avere accesso in lettura al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1afa6-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="1afa6-111">Per i token Hub molto il criterio fa parte della SAS.</span><span class="sxs-lookup"><span data-stu-id="1afa6-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="1afa6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1afa6-112">EXAMPLES</span></span>

### <span data-ttu-id="1afa6-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1afa6-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="1afa6-114">Genera un token SAS Hub molto con il criterio iothubowner e la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="1afa6-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="1afa6-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1afa6-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="1afa6-116">Genera un token SAS Hub molto con il criterio registryRead e la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="1afa6-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="1afa6-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1afa6-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="1afa6-118">Genera un token SAS del dispositivo usando i criteri di iothubowner per accedere al registro di sistema {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="1afa6-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="1afa6-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1afa6-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="1afa6-120">Genera un token SAS modulo usando i criteri di iothubowner per accedere al registro di sistema {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="1afa6-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="1afa6-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1afa6-121">PARAMETERS</span></span>

### <span data-ttu-id="1afa6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afa6-122">-DefaultProfile</span></span>
<span data-ttu-id="1afa6-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1afa6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1afa6-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1afa6-124">-DeviceId</span></span>
<span data-ttu-id="1afa6-125">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1afa6-125">Target Device Id.</span></span>

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

### <span data-ttu-id="1afa6-126">-Durata</span><span class="sxs-lookup"><span data-stu-id="1afa6-126">-Duration</span></span>
<span data-ttu-id="1afa6-127">Scadenza futura (in secondi) del token da generare.</span><span class="sxs-lookup"><span data-stu-id="1afa6-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="1afa6-128">Il valore predefinito è 3600.</span><span class="sxs-lookup"><span data-stu-id="1afa6-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afa6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1afa6-129">-InputObject</span></span>
<span data-ttu-id="1afa6-130">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="1afa6-130">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1afa6-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1afa6-131">-IotHubName</span></span>
<span data-ttu-id="1afa6-132">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="1afa6-132">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afa6-133">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="1afa6-133">-KeyName</span></span>
<span data-ttu-id="1afa6-134">Nome chiave di accesso.</span><span class="sxs-lookup"><span data-stu-id="1afa6-134">Access key name.</span></span>

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

### <span data-ttu-id="1afa6-135">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="1afa6-135">-KeyType</span></span>
<span data-ttu-id="1afa6-136">Tipo di chiave di accesso.</span><span class="sxs-lookup"><span data-stu-id="1afa6-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afa6-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="1afa6-137">-ModuleId</span></span>
<span data-ttu-id="1afa6-138">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1afa6-138">Target Module Id.</span></span>

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

### <span data-ttu-id="1afa6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1afa6-139">-ResourceGroupName</span></span>
<span data-ttu-id="1afa6-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1afa6-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afa6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1afa6-141">-ResourceId</span></span>
<span data-ttu-id="1afa6-142">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="1afa6-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afa6-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1afa6-143">-Confirm</span></span>
<span data-ttu-id="1afa6-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1afa6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afa6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afa6-145">-WhatIf</span></span>
<span data-ttu-id="1afa6-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1afa6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1afa6-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1afa6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afa6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afa6-148">CommonParameters</span></span>
<span data-ttu-id="1afa6-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afa6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afa6-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afa6-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afa6-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1afa6-151">INPUTS</span></span>

### <span data-ttu-id="1afa6-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1afa6-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1afa6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1afa6-153">System.String</span></span>

## <span data-ttu-id="1afa6-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1afa6-154">OUTPUTS</span></span>

### <span data-ttu-id="1afa6-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1afa6-155">System.String</span></span>

## <span data-ttu-id="1afa6-156">Note</span><span class="sxs-lookup"><span data-stu-id="1afa6-156">NOTES</span></span>

## <span data-ttu-id="1afa6-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1afa6-157">RELATED LINKS</span></span>
