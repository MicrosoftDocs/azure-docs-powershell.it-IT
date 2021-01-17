---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486292"
---
# <span data-ttu-id="5b73e-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b73e-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="5b73e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b73e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b73e-103">Eliminare il gruppo di sicurezza del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5b73e-103">Delete device security group</span></span>

## <span data-ttu-id="5b73e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b73e-104">SYNTAX</span></span>

### <span data-ttu-id="5b73e-105">ResourceIdLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b73e-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b73e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5b73e-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b73e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b73e-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b73e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b73e-108">DESCRIPTION</span></span>
<span data-ttu-id="5b73e-109">Il cmdlet Remove-AzDeviceSecurityGroup Elimina un gruppo di sicurezza dei dispositivi definito nella soluzione di sicurezza degli altri.</span><span class="sxs-lookup"><span data-stu-id="5b73e-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="5b73e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b73e-110">EXAMPLES</span></span>

### <span data-ttu-id="5b73e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b73e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="5b73e-112">Eliminare il gruppo di sicurezza dei dispositivi "MySecurityGroup" dell'hub degli Stati con ID risorsa "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="5b73e-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="5b73e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b73e-113">PARAMETERS</span></span>

### <span data-ttu-id="5b73e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b73e-114">-DefaultProfile</span></span>
<span data-ttu-id="5b73e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b73e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b73e-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="5b73e-116">-HubResourceId</span></span>
<span data-ttu-id="5b73e-117">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="5b73e-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b73e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b73e-118">-InputObject</span></span>
<span data-ttu-id="5b73e-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="5b73e-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b73e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b73e-120">-Name</span></span>
<span data-ttu-id="5b73e-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b73e-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b73e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b73e-122">-PassThru</span></span>
<span data-ttu-id="5b73e-123">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="5b73e-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5b73e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b73e-124">-ResourceId</span></span>
<span data-ttu-id="5b73e-125">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="5b73e-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b73e-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b73e-126">-Confirm</span></span>
<span data-ttu-id="5b73e-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b73e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b73e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b73e-128">-WhatIf</span></span>
<span data-ttu-id="5b73e-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b73e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b73e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b73e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b73e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b73e-131">CommonParameters</span></span>
<span data-ttu-id="5b73e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b73e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b73e-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b73e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b73e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b73e-134">INPUTS</span></span>

### <span data-ttu-id="5b73e-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b73e-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="5b73e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5b73e-136">System.String</span></span>

## <span data-ttu-id="5b73e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b73e-137">OUTPUTS</span></span>

### <span data-ttu-id="5b73e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b73e-138">System.Boolean</span></span>

## <span data-ttu-id="5b73e-139">Note</span><span class="sxs-lookup"><span data-stu-id="5b73e-139">NOTES</span></span>

## <span data-ttu-id="5b73e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b73e-140">RELATED LINKS</span></span>
