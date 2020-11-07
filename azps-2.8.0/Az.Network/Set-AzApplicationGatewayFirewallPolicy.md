---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852650"
---
# <span data-ttu-id="f7601-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7601-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="f7601-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7601-102">SYNOPSIS</span></span>
<span data-ttu-id="f7601-103">Aggiorna un criterio firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7601-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="f7601-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7601-104">SYNTAX</span></span>

### <span data-ttu-id="f7601-105">ByFactoryObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7601-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7601-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="f7601-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7601-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7601-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7601-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7601-108">DESCRIPTION</span></span>
<span data-ttu-id="f7601-109">Il cmdlet **set-AzApplicationGatewayFirewallPolicy** aggiorna un criterio firewall di Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7601-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="f7601-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7601-110">EXAMPLES</span></span>

### <span data-ttu-id="f7601-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7601-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="f7601-112">Questo comando Aggiorna i criteri del firewall del gateway applicazione con le impostazioni nella variabile $AppGwFirewallPolicy e archivia il gateway aggiornato nella variabile $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7601-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="f7601-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7601-113">PARAMETERS</span></span>

### <span data-ttu-id="f7601-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7601-114">-AsJob</span></span>
<span data-ttu-id="f7601-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7601-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7601-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="f7601-116">-CustomRule</span></span>
<span data-ttu-id="f7601-117">Elenco di CustomRules</span><span class="sxs-lookup"><span data-stu-id="f7601-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="f7601-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7601-118">-DefaultProfile</span></span>
<span data-ttu-id="f7601-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7601-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7601-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7601-120">-InputObject</span></span>
<span data-ttu-id="f7601-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7601-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="f7601-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7601-122">-Name</span></span>
<span data-ttu-id="f7601-123">Nome del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="f7601-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7601-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7601-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7601-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7601-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7601-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7601-126">-ResourceId</span></span>
<span data-ttu-id="f7601-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7601-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f7601-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7601-128">CommonParameters</span></span>
<span data-ttu-id="f7601-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7601-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7601-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7601-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7601-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7601-131">INPUTS</span></span>

### <span data-ttu-id="f7601-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7601-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="f7601-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7601-133">OUTPUTS</span></span>

### <span data-ttu-id="f7601-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7601-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="f7601-135">Note</span><span class="sxs-lookup"><span data-stu-id="f7601-135">NOTES</span></span>

## <span data-ttu-id="f7601-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7601-136">RELATED LINKS</span></span>
