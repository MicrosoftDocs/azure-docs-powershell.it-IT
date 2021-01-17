---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473917"
---
# <span data-ttu-id="415b7-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="415b7-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="415b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="415b7-102">SYNOPSIS</span></span>
<span data-ttu-id="415b7-103">Rigenera la chiave di accesso condivisa per un dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="415b7-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="415b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="415b7-104">SYNTAX</span></span>

### <span data-ttu-id="415b7-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="415b7-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="415b7-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="415b7-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="415b7-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="415b7-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415b7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b7-108">DESCRIPTION</span></span>
<span data-ttu-id="415b7-109">Rigenera la chiave di accesso condivisa per un dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="415b7-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="415b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="415b7-110">EXAMPLES</span></span>

### <span data-ttu-id="415b7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="415b7-111">Example 1</span></span>

<span data-ttu-id="415b7-112">Rigenerare la chiave corrispondente alla chiave \' Key1' \ del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="415b7-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="415b7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="415b7-113">Example 2</span></span>

<span data-ttu-id="415b7-114">Rigenerare la chiave corrispondente alla chiave \' Key1' \ del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="415b7-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="415b7-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="415b7-115">Example 3</span></span>

<span data-ttu-id="415b7-116">Rigenerare la chiave corrispondente alla chiave \' Key2' \ of Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` usando il relativo ID risorsa completo.</span><span class="sxs-lookup"><span data-stu-id="415b7-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="415b7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="415b7-117">PARAMETERS</span></span>

### <span data-ttu-id="415b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415b7-118">-DefaultProfile</span></span>
<span data-ttu-id="415b7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="415b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="415b7-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="415b7-120">-DomainInputObject</span></span>
<span data-ttu-id="415b7-121">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="415b7-121">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="415b7-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="415b7-122">-DomainName</span></span>
<span data-ttu-id="415b7-123">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="415b7-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415b7-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="415b7-124">-DomainResourceId</span></span>
<span data-ttu-id="415b7-125">Identificatore delle risorse che rappresenta il dominio della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="415b7-125">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415b7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="415b7-126">-Name</span></span>
<span data-ttu-id="415b7-127">Nome della chiave che deve essere rigenerata</span><span class="sxs-lookup"><span data-stu-id="415b7-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="415b7-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="415b7-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415b7-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="415b7-130">-Confirm</span></span>
<span data-ttu-id="415b7-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="415b7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415b7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415b7-132">-WhatIf</span></span>
<span data-ttu-id="415b7-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="415b7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415b7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="415b7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415b7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415b7-135">CommonParameters</span></span>
<span data-ttu-id="415b7-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415b7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415b7-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="415b7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415b7-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="415b7-138">INPUTS</span></span>

### <span data-ttu-id="415b7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="415b7-139">System.String</span></span>

### <span data-ttu-id="415b7-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="415b7-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="415b7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="415b7-141">OUTPUTS</span></span>

### <span data-ttu-id="415b7-142">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="415b7-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="415b7-143">Note</span><span class="sxs-lookup"><span data-stu-id="415b7-143">NOTES</span></span>

## <span data-ttu-id="415b7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="415b7-144">RELATED LINKS</span></span>
