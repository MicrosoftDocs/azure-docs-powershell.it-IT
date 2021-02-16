---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178934"
---
# <span data-ttu-id="fae4e-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fae4e-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="fae4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae4e-102">SYNOPSIS</span></span>
<span data-ttu-id="fae4e-103">Rimuove la regola di autorizzazione di hybridConnection dalle entità di inoltro fornite (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fae4e-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fae4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fae4e-104">SYNTAX</span></span>

### <span data-ttu-id="fae4e-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fae4e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae4e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fae4e-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fae4e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fae4e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae4e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fae4e-108">DESCRIPTION</span></span>
<span data-ttu-id="fae4e-109">Il cmdlet **Remove-AzRelayAuthorizationRule** rimuove la regola di autorizzazione delle entità di inoltro fornite (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fae4e-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fae4e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fae4e-110">EXAMPLES</span></span>

### <span data-ttu-id="fae4e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fae4e-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="fae4e-112">Rimuove la regola di autorizzazione `AuthoRule1` dello spazio dei `TestNameSpace-Relay1` nomi.</span><span class="sxs-lookup"><span data-stu-id="fae4e-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="fae4e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fae4e-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="fae4e-114">Rimuove la regola di `AuthoRule1` autorizzazione di WcfRelay `TestWcfRelay` dallo spazio dei `TestNameSpace-Relay1` nomi.</span><span class="sxs-lookup"><span data-stu-id="fae4e-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="fae4e-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fae4e-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="fae4e-116">Rimuove la regola di `AuthoRule1` autorizzazione di HybridConnection `TestHybridConnection` dallo spazio dei `TestNameSpace-Relay1` nomi.</span><span class="sxs-lookup"><span data-stu-id="fae4e-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="fae4e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fae4e-117">PARAMETERS</span></span>

### <span data-ttu-id="fae4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae4e-118">-DefaultProfile</span></span>
<span data-ttu-id="fae4e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fae4e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae4e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fae4e-120">-Force</span></span>
<span data-ttu-id="fae4e-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="fae4e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fae4e-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fae4e-122">-HybridConnection</span></span>
<span data-ttu-id="fae4e-123">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="fae4e-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae4e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fae4e-124">-Name</span></span>
<span data-ttu-id="fae4e-125">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="fae4e-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae4e-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fae4e-126">-Namespace</span></span>
<span data-ttu-id="fae4e-127">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fae4e-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae4e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fae4e-128">-PassThru</span></span>
<span data-ttu-id="fae4e-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fae4e-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fae4e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae4e-130">-ResourceGroupName</span></span>
<span data-ttu-id="fae4e-131">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fae4e-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae4e-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fae4e-132">-WcfRelay</span></span>
<span data-ttu-id="fae4e-133">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fae4e-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae4e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fae4e-134">-Confirm</span></span>
<span data-ttu-id="fae4e-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fae4e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae4e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae4e-136">-WhatIf</span></span>
<span data-ttu-id="fae4e-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fae4e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae4e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fae4e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae4e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae4e-139">CommonParameters</span></span>
<span data-ttu-id="fae4e-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae4e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae4e-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae4e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae4e-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="fae4e-142">INPUTS</span></span>

### <span data-ttu-id="fae4e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fae4e-143">System.String</span></span>

## <span data-ttu-id="fae4e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fae4e-144">OUTPUTS</span></span>

### <span data-ttu-id="fae4e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fae4e-145">System.Boolean</span></span>

## <span data-ttu-id="fae4e-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="fae4e-146">NOTES</span></span>

## <span data-ttu-id="fae4e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fae4e-147">RELATED LINKS</span></span>
