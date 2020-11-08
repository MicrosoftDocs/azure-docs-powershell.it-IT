---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020468"
---
# <span data-ttu-id="7dba9-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7dba9-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="7dba9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7dba9-102">SYNOPSIS</span></span>
<span data-ttu-id="7dba9-103">Salva un criterio firewall di Azure modificato</span><span class="sxs-lookup"><span data-stu-id="7dba9-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="7dba9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dba9-104">SYNTAX</span></span>

### <span data-ttu-id="7dba9-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7dba9-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dba9-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dba9-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dba9-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dba9-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dba9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dba9-108">DESCRIPTION</span></span>
<span data-ttu-id="7dba9-109">Il cmdlet **set-AzFirewallPolicy** aggiorna i criteri di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="7dba9-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="7dba9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dba9-110">EXAMPLES</span></span>

### <span data-ttu-id="7dba9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7dba9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="7dba9-112">Questo esempio imposta i criteri del firewall con il nuovo valore dei criteri firewall</span><span class="sxs-lookup"><span data-stu-id="7dba9-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="7dba9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7dba9-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="7dba9-114">Questo esempio imposta i criteri del firewall con la nuova modalità Intel Threat</span><span class="sxs-lookup"><span data-stu-id="7dba9-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="7dba9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7dba9-115">PARAMETERS</span></span>

### <span data-ttu-id="7dba9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dba9-116">-AsJob</span></span>
<span data-ttu-id="7dba9-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7dba9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dba9-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="7dba9-118">-BasePolicy</span></span>
<span data-ttu-id="7dba9-119">Criteri di base per cui ereditare da</span><span class="sxs-lookup"><span data-stu-id="7dba9-119">The base policy to inherit from</span></span>

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

### <span data-ttu-id="7dba9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dba9-120">-DefaultProfile</span></span>
<span data-ttu-id="7dba9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dba9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dba9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dba9-122">-InputObject</span></span>
<span data-ttu-id="7dba9-123">Criteri AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7dba9-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dba9-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7dba9-124">-Location</span></span>
<span data-ttu-id="7dba9-125">posizione.</span><span class="sxs-lookup"><span data-stu-id="7dba9-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dba9-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dba9-126">-Name</span></span>
<span data-ttu-id="7dba9-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7dba9-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dba9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dba9-128">-ResourceGroupName</span></span>
<span data-ttu-id="7dba9-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7dba9-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dba9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dba9-130">-ResourceId</span></span>
<span data-ttu-id="7dba9-131">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7dba9-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dba9-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="7dba9-132">-Tag</span></span>
<span data-ttu-id="7dba9-133">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7dba9-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7dba9-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="7dba9-134">-ThreatIntelMode</span></span>
<span data-ttu-id="7dba9-135">Modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="7dba9-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dba9-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7dba9-136">-Confirm</span></span>
<span data-ttu-id="7dba9-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dba9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dba9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dba9-138">-WhatIf</span></span>
<span data-ttu-id="7dba9-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dba9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dba9-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dba9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dba9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dba9-141">CommonParameters</span></span>
<span data-ttu-id="7dba9-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dba9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dba9-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dba9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dba9-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7dba9-144">INPUTS</span></span>

### <span data-ttu-id="7dba9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7dba9-145">System.String</span></span>

### <span data-ttu-id="7dba9-146">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7dba9-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="7dba9-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7dba9-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7dba9-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dba9-148">OUTPUTS</span></span>

### <span data-ttu-id="7dba9-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7dba9-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7dba9-150">Note</span><span class="sxs-lookup"><span data-stu-id="7dba9-150">NOTES</span></span>

## <span data-ttu-id="7dba9-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dba9-151">RELATED LINKS</span></span>
