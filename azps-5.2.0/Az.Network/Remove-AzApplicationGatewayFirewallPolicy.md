---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345892"
---
# <span data-ttu-id="4462b-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4462b-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="4462b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4462b-102">SYNOPSIS</span></span>
<span data-ttu-id="4462b-103">Rimuove un criterio del firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4462b-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="4462b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4462b-104">SYNTAX</span></span>

### <span data-ttu-id="4462b-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4462b-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4462b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4462b-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4462b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4462b-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4462b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4462b-108">DESCRIPTION</span></span>
<span data-ttu-id="4462b-109">Il cmdlet **Remove-AzApplicationGatewayFirewallPolicy** rimuove i criteri del firewall di gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4462b-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="4462b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4462b-110">EXAMPLES</span></span>

### <span data-ttu-id="4462b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4462b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4462b-112">Questo comando consente di rimuovere i criteri del firewall gateway applicazione denominati ApplicationGatewayFirewallPolicy01 nel gruppo risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4462b-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4462b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4462b-113">PARAMETERS</span></span>

### <span data-ttu-id="4462b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4462b-114">-AsJob</span></span>
<span data-ttu-id="4462b-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4462b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4462b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4462b-116">-DefaultProfile</span></span>
<span data-ttu-id="4462b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4462b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4462b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4462b-118">-Force</span></span>
<span data-ttu-id="4462b-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4462b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4462b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4462b-120">-InputObject</span></span>
<span data-ttu-id="4462b-121">Oggetto criteri firewall</span><span class="sxs-lookup"><span data-stu-id="4462b-121">The firewall policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4462b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4462b-122">-Name</span></span>
<span data-ttu-id="4462b-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4462b-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4462b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4462b-124">-PassThru</span></span>
<span data-ttu-id="4462b-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4462b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4462b-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4462b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4462b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4462b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4462b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4462b-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4462b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4462b-129">-ResourceId</span></span>
<span data-ttu-id="4462b-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="4462b-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4462b-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4462b-131">-Confirm</span></span>
<span data-ttu-id="4462b-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4462b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4462b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4462b-133">-WhatIf</span></span>
<span data-ttu-id="4462b-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4462b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4462b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4462b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4462b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4462b-136">CommonParameters</span></span>
<span data-ttu-id="4462b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4462b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4462b-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4462b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4462b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4462b-139">INPUTS</span></span>

### <span data-ttu-id="4462b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4462b-140">System.String</span></span>

## <span data-ttu-id="4462b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4462b-141">OUTPUTS</span></span>

### <span data-ttu-id="4462b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4462b-142">System.Boolean</span></span>

## <span data-ttu-id="4462b-143">Note</span><span class="sxs-lookup"><span data-stu-id="4462b-143">NOTES</span></span>

## <span data-ttu-id="4462b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4462b-144">RELATED LINKS</span></span>
