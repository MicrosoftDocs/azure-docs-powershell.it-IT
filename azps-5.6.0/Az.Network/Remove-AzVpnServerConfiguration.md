---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: f5451b2c3af331f0086f39f46028aff1d33bf002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990007"
---
# <span data-ttu-id="2458a-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2458a-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="2458a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2458a-102">SYNOPSIS</span></span>
<span data-ttu-id="2458a-103">Rimuove una VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="2458a-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="2458a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2458a-104">SYNTAX</span></span>

### <span data-ttu-id="2458a-105">ByVpnServerConfigurationName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2458a-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2458a-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2458a-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2458a-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="2458a-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2458a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2458a-108">DESCRIPTION</span></span>
<span data-ttu-id="2458a-109">{{Inserire la descrizione}}</span><span class="sxs-lookup"><span data-stu-id="2458a-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2458a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2458a-110">EXAMPLES</span></span>

### <span data-ttu-id="2458a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2458a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="2458a-112">Il comando precedente rimuoverà una VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="2458a-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="2458a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2458a-113">PARAMETERS</span></span>

### <span data-ttu-id="2458a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2458a-114">-DefaultProfile</span></span>
<span data-ttu-id="2458a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2458a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2458a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2458a-116">-Force</span></span>
<span data-ttu-id="2458a-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2458a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2458a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2458a-118">-InputObject</span></span>
<span data-ttu-id="2458a-119">Oggetto vpnServerConfiguration da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2458a-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2458a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2458a-120">-Name</span></span>
<span data-ttu-id="2458a-121">Nome vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2458a-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2458a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2458a-122">-PassThru</span></span>
<span data-ttu-id="2458a-123">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2458a-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2458a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2458a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2458a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2458a-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2458a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2458a-126">-ResourceId</span></span>
<span data-ttu-id="2458a-127">ID della risorsa Azure per la vpnServerConfiguration da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2458a-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2458a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2458a-128">-Confirm</span></span>
<span data-ttu-id="2458a-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2458a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2458a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2458a-130">-WhatIf</span></span>
<span data-ttu-id="2458a-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2458a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2458a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2458a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2458a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2458a-133">CommonParameters</span></span>
<span data-ttu-id="2458a-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2458a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2458a-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2458a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2458a-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="2458a-136">INPUTS</span></span>

### <span data-ttu-id="2458a-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2458a-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="2458a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2458a-138">System.String</span></span>

## <span data-ttu-id="2458a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2458a-139">OUTPUTS</span></span>

### <span data-ttu-id="2458a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2458a-140">System.Boolean</span></span>

## <span data-ttu-id="2458a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="2458a-141">NOTES</span></span>

## <span data-ttu-id="2458a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2458a-142">RELATED LINKS</span></span>
