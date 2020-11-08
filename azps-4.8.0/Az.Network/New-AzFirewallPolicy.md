---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192798"
---
# <span data-ttu-id="30d95-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="30d95-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="30d95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30d95-102">SYNOPSIS</span></span>
<span data-ttu-id="30d95-103">Crea un nuovo criterio di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="30d95-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="30d95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30d95-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30d95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30d95-105">DESCRIPTION</span></span>
<span data-ttu-id="30d95-106">Il cmdlet **New-AzFirewallPolicy** crea un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="30d95-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="30d95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30d95-107">EXAMPLES</span></span>

### <span data-ttu-id="30d95-108">Esempio 1:1.</span><span class="sxs-lookup"><span data-stu-id="30d95-108">Example 1: 1.</span></span> <span data-ttu-id="30d95-109">Creare un criterio vuoto</span><span class="sxs-lookup"><span data-stu-id="30d95-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="30d95-110">Questo esempio crea un criterio di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="30d95-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="30d95-111">Esempio 2:2.</span><span class="sxs-lookup"><span data-stu-id="30d95-111">Example 2: 2.</span></span> <span data-ttu-id="30d95-112">Creare un criterio vuoto con la modalità ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="30d95-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="30d95-113">Questo esempio crea un criterio di Azure Firewall con una modalità Intel per le minacce</span><span class="sxs-lookup"><span data-stu-id="30d95-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="30d95-114">Esempio 3:3.</span><span class="sxs-lookup"><span data-stu-id="30d95-114">Example 3: 3.</span></span> <span data-ttu-id="30d95-115">Creare un criterio vuoto con ThreatIntel whitelist</span><span class="sxs-lookup"><span data-stu-id="30d95-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="30d95-116">Questo esempio crea un criterio di Azure Firewall con una minaccia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="30d95-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="30d95-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30d95-117">PARAMETERS</span></span>

### <span data-ttu-id="30d95-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30d95-118">-AsJob</span></span>
<span data-ttu-id="30d95-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="30d95-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30d95-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="30d95-120">-BasePolicy</span></span>
<span data-ttu-id="30d95-121">Criteri di base per cui ereditare da</span><span class="sxs-lookup"><span data-stu-id="30d95-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d95-122">-DefaultProfile</span></span>
<span data-ttu-id="30d95-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30d95-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30d95-124">-Force</span><span class="sxs-lookup"><span data-stu-id="30d95-124">-Force</span></span>
<span data-ttu-id="30d95-125">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="30d95-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="30d95-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="30d95-126">-Location</span></span>
<span data-ttu-id="30d95-127">posizione.</span><span class="sxs-lookup"><span data-stu-id="30d95-127">location.</span></span>

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

### <span data-ttu-id="30d95-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="30d95-128">-Name</span></span>
<span data-ttu-id="30d95-129">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="30d95-129">The resource name.</span></span>

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

### <span data-ttu-id="30d95-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d95-130">-ResourceGroupName</span></span>
<span data-ttu-id="30d95-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30d95-131">The resource group name.</span></span>

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

### <span data-ttu-id="30d95-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="30d95-132">-Tag</span></span>
<span data-ttu-id="30d95-133">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="30d95-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="30d95-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="30d95-134">-ThreatIntelMode</span></span>
<span data-ttu-id="30d95-135">Modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="30d95-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="30d95-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="30d95-137">Whitelist per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="30d95-137">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="30d95-138">-DnsSetting</span></span>
<span data-ttu-id="30d95-139">Impostazione DNS</span><span class="sxs-lookup"><span data-stu-id="30d95-139">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30d95-140">-Confirm</span></span>
<span data-ttu-id="30d95-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30d95-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d95-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d95-142">-WhatIf</span></span>
<span data-ttu-id="30d95-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30d95-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d95-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30d95-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d95-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d95-145">CommonParameters</span></span>
<span data-ttu-id="30d95-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d95-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d95-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30d95-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d95-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30d95-148">INPUTS</span></span>

### <span data-ttu-id="30d95-149">System. String</span><span class="sxs-lookup"><span data-stu-id="30d95-149">System.String</span></span>

### <span data-ttu-id="30d95-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="30d95-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30d95-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30d95-151">OUTPUTS</span></span>

### <span data-ttu-id="30d95-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="30d95-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="30d95-153">Note</span><span class="sxs-lookup"><span data-stu-id="30d95-153">NOTES</span></span>

## <span data-ttu-id="30d95-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30d95-154">RELATED LINKS</span></span>
