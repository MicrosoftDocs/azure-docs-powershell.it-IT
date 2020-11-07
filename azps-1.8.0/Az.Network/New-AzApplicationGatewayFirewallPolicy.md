---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 6813bf30da73f09f285151d6d309eb89b32acbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678370"
---
# <span data-ttu-id="12ea9-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="12ea9-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="12ea9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="12ea9-103">Crea un criterio firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="12ea9-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="12ea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ea9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ea9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="12ea9-106">Il cmdlet **New-AzApplicationGatewayFirewallPolicy** crea un criterio del firewall di gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="12ea9-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="12ea9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="12ea9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12ea9-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzureRmApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="12ea9-109">Questo comando crea un nuovo criterio firewall di gateway di applicazioni di Azure denominato "wafResource1" nel gruppo di risorse "RG1" in location "westus" con le regole personalizzate definite nella variabile $customRule</span><span class="sxs-lookup"><span data-stu-id="12ea9-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="12ea9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12ea9-110">PARAMETERS</span></span>

### <span data-ttu-id="12ea9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12ea9-111">-AsJob</span></span>
<span data-ttu-id="12ea9-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12ea9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12ea9-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="12ea9-113">-CustomRule</span></span>
<span data-ttu-id="12ea9-114">Elenco di CustomRules</span><span class="sxs-lookup"><span data-stu-id="12ea9-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ea9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ea9-115">-DefaultProfile</span></span>
<span data-ttu-id="12ea9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12ea9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ea9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="12ea9-117">-Force</span></span>
<span data-ttu-id="12ea9-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="12ea9-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="12ea9-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="12ea9-119">-Location</span></span>
<span data-ttu-id="12ea9-120">posizione.</span><span class="sxs-lookup"><span data-stu-id="12ea9-120">location.</span></span>

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

### <span data-ttu-id="12ea9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="12ea9-121">-Name</span></span>
<span data-ttu-id="12ea9-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="12ea9-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ea9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ea9-123">-ResourceGroupName</span></span>
<span data-ttu-id="12ea9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12ea9-124">The resource group name.</span></span>

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

### <span data-ttu-id="12ea9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="12ea9-125">-Tag</span></span>
<span data-ttu-id="12ea9-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="12ea9-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="12ea9-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12ea9-127">-Confirm</span></span>
<span data-ttu-id="12ea9-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ea9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ea9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ea9-129">-WhatIf</span></span>
<span data-ttu-id="12ea9-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ea9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12ea9-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ea9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ea9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ea9-132">CommonParameters</span></span>
<span data-ttu-id="12ea9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ea9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ea9-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ea9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ea9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12ea9-135">INPUTS</span></span>

### <span data-ttu-id="12ea9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="12ea9-136">System.String</span></span>

### <span data-ttu-id="12ea9-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="12ea9-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="12ea9-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="12ea9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="12ea9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ea9-139">OUTPUTS</span></span>

### <span data-ttu-id="12ea9-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="12ea9-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="12ea9-141">Note</span><span class="sxs-lookup"><span data-stu-id="12ea9-141">NOTES</span></span>

## <span data-ttu-id="12ea9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ea9-142">RELATED LINKS</span></span>
