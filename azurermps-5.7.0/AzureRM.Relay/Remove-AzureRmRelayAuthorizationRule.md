---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 62d37b30f20cf6d0738cfc927c266d6869be5586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686702"
---
# <span data-ttu-id="44365-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44365-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="44365-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44365-102">SYNOPSIS</span></span>
<span data-ttu-id="44365-103">Rimuove la regola di autorizzazione di un HybridConnection dalle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="44365-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44365-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44365-104">SYNTAX</span></span>

### <span data-ttu-id="44365-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44365-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44365-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="44365-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44365-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="44365-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44365-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44365-108">DESCRIPTION</span></span>
<span data-ttu-id="44365-109">Il cmdlet **Remove-AzureRmRelayAuthorizationRule** rimuove la regola di autorizzazione delle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="44365-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="44365-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44365-110">EXAMPLES</span></span>

### <span data-ttu-id="44365-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44365-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="44365-112">Rimuove la regola `AuthoRule1` di autorizzazione dello spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="44365-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="44365-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="44365-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="44365-114">Rimuove la regola `AuthoRule1` di autorizzazione di WcfRelay `TestWcfRelay` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="44365-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="44365-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="44365-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="44365-116">Rimuove la regola `AuthoRule1` di autorizzazione di HybridConnection `TestHybridConnection` dallo spazio dei nomi `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="44365-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="44365-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44365-117">PARAMETERS</span></span>

### <span data-ttu-id="44365-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44365-118">-DefaultProfile</span></span>
<span data-ttu-id="44365-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44365-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44365-120">-Force</span><span class="sxs-lookup"><span data-stu-id="44365-120">-Force</span></span>
<span data-ttu-id="44365-121">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="44365-121">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="44365-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="44365-122">-HybridConnection</span></span>
<span data-ttu-id="44365-123">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="44365-123">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44365-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="44365-124">-Name</span></span>
<span data-ttu-id="44365-125">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="44365-125">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44365-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="44365-126">-Namespace</span></span>
<span data-ttu-id="44365-127">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="44365-127">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44365-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44365-128">-PassThru</span></span>
<span data-ttu-id="44365-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="44365-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="44365-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44365-130">-ResourceGroupName</span></span>
<span data-ttu-id="44365-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44365-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44365-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="44365-132">-WcfRelay</span></span>
<span data-ttu-id="44365-133">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="44365-133">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44365-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44365-134">-Confirm</span></span>
<span data-ttu-id="44365-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44365-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44365-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44365-136">-WhatIf</span></span>
<span data-ttu-id="44365-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44365-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44365-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44365-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44365-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44365-139">CommonParameters</span></span>
<span data-ttu-id="44365-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44365-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44365-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44365-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44365-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44365-142">INPUTS</span></span>

### <span data-ttu-id="44365-143">System. String</span><span class="sxs-lookup"><span data-stu-id="44365-143">System.String</span></span>

## <span data-ttu-id="44365-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44365-144">OUTPUTS</span></span>

### <span data-ttu-id="44365-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44365-145">System.Boolean</span></span>

## <span data-ttu-id="44365-146">Note</span><span class="sxs-lookup"><span data-stu-id="44365-146">NOTES</span></span>

## <span data-ttu-id="44365-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44365-147">RELATED LINKS</span></span>

