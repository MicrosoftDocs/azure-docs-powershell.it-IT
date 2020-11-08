---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192073"
---
# <span data-ttu-id="e95fd-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e95fd-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="e95fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e95fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e95fd-103">Crea un SecurityPartnerProvider di Azure.</span><span class="sxs-lookup"><span data-stu-id="e95fd-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="e95fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e95fd-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e95fd-105">DESCRIPTION</span></span>
<span data-ttu-id="e95fd-106">Il cmdlet **New-AzSecurityPartnerProvider** crea un SecurityPartnerProvider di Azure</span><span class="sxs-lookup"><span data-stu-id="e95fd-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="e95fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e95fd-107">EXAMPLES</span></span>

### <span data-ttu-id="e95fd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e95fd-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="e95fd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e95fd-109">PARAMETERS</span></span>

### <span data-ttu-id="e95fd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e95fd-110">-AsJob</span></span>
<span data-ttu-id="e95fd-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e95fd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95fd-112">-DefaultProfile</span></span>
<span data-ttu-id="e95fd-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e95fd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95fd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e95fd-114">-Force</span></span>
<span data-ttu-id="e95fd-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="e95fd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e95fd-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e95fd-116">-Location</span></span>
<span data-ttu-id="e95fd-117">posizione.</span><span class="sxs-lookup"><span data-stu-id="e95fd-117">location.</span></span>

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

### <span data-ttu-id="e95fd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e95fd-118">-Name</span></span>
<span data-ttu-id="e95fd-119">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e95fd-119">The resource name.</span></span>

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

### <span data-ttu-id="e95fd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95fd-120">-ResourceGroupName</span></span>
<span data-ttu-id="e95fd-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e95fd-121">The resource group name.</span></span>

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

### <span data-ttu-id="e95fd-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="e95fd-122">-SecurityProviderName</span></span>
<span data-ttu-id="e95fd-123">Nome del provider di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e95fd-123">The Security Provider name</span></span>

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

### <span data-ttu-id="e95fd-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="e95fd-124">-Tag</span></span>
<span data-ttu-id="e95fd-125">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e95fd-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e95fd-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e95fd-126">-VirtualHub</span></span>
<span data-ttu-id="e95fd-127">ID hub virtuale a cui è associato il provider del partner di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e95fd-127">The virtual hub Id that the security partner provider is attached to</span></span>

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

### <span data-ttu-id="e95fd-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="e95fd-128">-VirtualHubId</span></span>
<span data-ttu-id="e95fd-129">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e95fd-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="e95fd-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="e95fd-130">-VirtualHubName</span></span>
<span data-ttu-id="e95fd-131">ID dell'VirtualHub a cui deve essere associato questo VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e95fd-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="e95fd-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e95fd-132">-Confirm</span></span>
<span data-ttu-id="e95fd-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95fd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95fd-134">-WhatIf</span></span>
<span data-ttu-id="e95fd-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e95fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95fd-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e95fd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95fd-137">CommonParameters</span></span>
<span data-ttu-id="e95fd-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95fd-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e95fd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95fd-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e95fd-140">INPUTS</span></span>

### <span data-ttu-id="e95fd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e95fd-141">System.String</span></span>

### <span data-ttu-id="e95fd-142">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e95fd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e95fd-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e95fd-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e95fd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e95fd-144">OUTPUTS</span></span>

### <span data-ttu-id="e95fd-145">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e95fd-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="e95fd-146">Note</span><span class="sxs-lookup"><span data-stu-id="e95fd-146">NOTES</span></span>

## <span data-ttu-id="e95fd-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e95fd-147">RELATED LINKS</span></span>
