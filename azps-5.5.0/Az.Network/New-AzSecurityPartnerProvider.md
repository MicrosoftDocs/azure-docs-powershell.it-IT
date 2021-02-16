---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179615"
---
# <span data-ttu-id="65f13-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="65f13-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="65f13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f13-102">SYNOPSIS</span></span>
<span data-ttu-id="65f13-103">Crea un Provider SecurityPartnerProvider di Azure.</span><span class="sxs-lookup"><span data-stu-id="65f13-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="65f13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65f13-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65f13-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65f13-105">DESCRIPTION</span></span>
<span data-ttu-id="65f13-106">Il cmdlet **New-AzSecurityPartnerProvider crea** un Provider SecurityPartner di Azure</span><span class="sxs-lookup"><span data-stu-id="65f13-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="65f13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65f13-107">EXAMPLES</span></span>

### <span data-ttu-id="65f13-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65f13-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="65f13-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65f13-109">PARAMETERS</span></span>

### <span data-ttu-id="65f13-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65f13-110">-AsJob</span></span>
<span data-ttu-id="65f13-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="65f13-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65f13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f13-112">-DefaultProfile</span></span>
<span data-ttu-id="65f13-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65f13-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f13-114">-Force</span><span class="sxs-lookup"><span data-stu-id="65f13-114">-Force</span></span>
<span data-ttu-id="65f13-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="65f13-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="65f13-116">-Location</span><span class="sxs-lookup"><span data-stu-id="65f13-116">-Location</span></span>
<span data-ttu-id="65f13-117">posizione.</span><span class="sxs-lookup"><span data-stu-id="65f13-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f13-118">-Name</span><span class="sxs-lookup"><span data-stu-id="65f13-118">-Name</span></span>
<span data-ttu-id="65f13-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="65f13-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f13-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65f13-120">-ResourceGroupName</span></span>
<span data-ttu-id="65f13-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65f13-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f13-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="65f13-122">-SecurityProviderName</span></span>
<span data-ttu-id="65f13-123">Nome del provider di sicurezza</span><span class="sxs-lookup"><span data-stu-id="65f13-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f13-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="65f13-124">-Tag</span></span>
<span data-ttu-id="65f13-125">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="65f13-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f13-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="65f13-126">-VirtualHub</span></span>
<span data-ttu-id="65f13-127">ID hub virtuale a cui è collegato il provider del partner di sicurezza</span><span class="sxs-lookup"><span data-stu-id="65f13-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65f13-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="65f13-128">-VirtualHubId</span></span>
<span data-ttu-id="65f13-129">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="65f13-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="65f13-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="65f13-130">-VirtualHubName</span></span>
<span data-ttu-id="65f13-131">ID di VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="65f13-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="65f13-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65f13-132">-Confirm</span></span>
<span data-ttu-id="65f13-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65f13-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65f13-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65f13-134">-WhatIf</span></span>
<span data-ttu-id="65f13-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65f13-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65f13-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65f13-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65f13-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f13-137">CommonParameters</span></span>
<span data-ttu-id="65f13-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f13-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f13-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65f13-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f13-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="65f13-140">INPUTS</span></span>

### <span data-ttu-id="65f13-141">System.String</span><span class="sxs-lookup"><span data-stu-id="65f13-141">System.String</span></span>

### <span data-ttu-id="65f13-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="65f13-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="65f13-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="65f13-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65f13-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65f13-144">OUTPUTS</span></span>

### <span data-ttu-id="65f13-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="65f13-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="65f13-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="65f13-146">NOTES</span></span>

## <span data-ttu-id="65f13-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65f13-147">RELATED LINKS</span></span>
