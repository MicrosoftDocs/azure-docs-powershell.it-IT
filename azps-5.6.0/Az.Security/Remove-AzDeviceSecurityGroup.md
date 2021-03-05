---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: 302e4b096c3a41c6dd5a57a87d23bf15b83c96a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984141"
---
# <span data-ttu-id="2eb11-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2eb11-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="2eb11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb11-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb11-103">Elimina gruppo di sicurezza del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2eb11-103">Delete device security group</span></span>

## <span data-ttu-id="2eb11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eb11-104">SYNTAX</span></span>

### <span data-ttu-id="2eb11-105">ResourceIdLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="2eb11-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb11-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2eb11-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb11-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb11-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb11-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2eb11-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb11-109">Il Remove-AzDeviceSecurityGroup elimina un gruppo di sicurezza dei dispositivi definito nella soluzione di sicurezza iot.</span><span class="sxs-lookup"><span data-stu-id="2eb11-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="2eb11-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eb11-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb11-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2eb11-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="2eb11-112">Eliminare il gruppo di sicurezza "MySecurityGroup" dell'hub iot con ID risorsa "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="2eb11-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="2eb11-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb11-113">PARAMETERS</span></span>

### <span data-ttu-id="2eb11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb11-114">-DefaultProfile</span></span>
<span data-ttu-id="2eb11-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb11-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb11-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb11-116">-HubResourceId</span></span>
<span data-ttu-id="2eb11-117">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="2eb11-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2eb11-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eb11-118">-InputObject</span></span>
<span data-ttu-id="2eb11-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="2eb11-119">Input Object.</span></span>

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

### <span data-ttu-id="2eb11-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb11-120">-Name</span></span>
<span data-ttu-id="2eb11-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2eb11-121">Resource name.</span></span>

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

### <span data-ttu-id="2eb11-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eb11-122">-PassThru</span></span>
<span data-ttu-id="2eb11-123">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="2eb11-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="2eb11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb11-124">-ResourceId</span></span>
<span data-ttu-id="2eb11-125">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="2eb11-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2eb11-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eb11-126">-Confirm</span></span>
<span data-ttu-id="2eb11-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb11-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb11-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb11-128">-WhatIf</span></span>
<span data-ttu-id="2eb11-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eb11-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb11-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eb11-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb11-131">CommonParameters</span></span>
<span data-ttu-id="2eb11-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb11-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2eb11-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb11-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2eb11-134">INPUTS</span></span>

### <span data-ttu-id="2eb11-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2eb11-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="2eb11-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2eb11-136">System.String</span></span>

## <span data-ttu-id="2eb11-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eb11-137">OUTPUTS</span></span>

### <span data-ttu-id="2eb11-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2eb11-138">System.Boolean</span></span>

## <span data-ttu-id="2eb11-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2eb11-139">NOTES</span></span>

## <span data-ttu-id="2eb11-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eb11-140">RELATED LINKS</span></span>
