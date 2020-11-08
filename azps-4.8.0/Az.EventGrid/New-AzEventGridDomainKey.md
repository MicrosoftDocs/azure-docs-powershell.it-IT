---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190745"
---
# <span data-ttu-id="a501b-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a501b-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="a501b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a501b-102">SYNOPSIS</span></span>
<span data-ttu-id="a501b-103">Rigenera la chiave di accesso condivisa per un dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a501b-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="a501b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a501b-104">SYNTAX</span></span>

### <span data-ttu-id="a501b-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a501b-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a501b-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a501b-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a501b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a501b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a501b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a501b-108">DESCRIPTION</span></span>
<span data-ttu-id="a501b-109">Rigenera la chiave di accesso condivisa per un dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a501b-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="a501b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a501b-110">EXAMPLES</span></span>

### <span data-ttu-id="a501b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a501b-111">Example 1</span></span>

<span data-ttu-id="a501b-112">Rigenerare la chiave corrispondente alla chiave \' Key1' \ del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a501b-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="a501b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a501b-113">Example 2</span></span>

<span data-ttu-id="a501b-114">Rigenerare la chiave corrispondente alla chiave \' Key1' \ del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a501b-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="a501b-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a501b-115">Example 3</span></span>

<span data-ttu-id="a501b-116">Rigenerare la chiave corrispondente alla chiave \' Key2' \ of Domain Grid \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` usando il relativo ID risorsa completo.</span><span class="sxs-lookup"><span data-stu-id="a501b-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="a501b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a501b-117">PARAMETERS</span></span>

### <span data-ttu-id="a501b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a501b-118">-DefaultProfile</span></span>
<span data-ttu-id="a501b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a501b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a501b-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a501b-120">-DomainInputObject</span></span>
<span data-ttu-id="a501b-121">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a501b-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a501b-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a501b-122">-DomainName</span></span>
<span data-ttu-id="a501b-123">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a501b-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="a501b-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="a501b-124">-DomainResourceId</span></span>
<span data-ttu-id="a501b-125">Identificatore delle risorse che rappresenta il dominio della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a501b-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="a501b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a501b-126">-Name</span></span>
<span data-ttu-id="a501b-127">Nome della chiave che deve essere rigenerata</span><span class="sxs-lookup"><span data-stu-id="a501b-127">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="a501b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a501b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a501b-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a501b-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="a501b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a501b-130">-Confirm</span></span>
<span data-ttu-id="a501b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a501b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a501b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a501b-132">-WhatIf</span></span>
<span data-ttu-id="a501b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a501b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a501b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a501b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a501b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a501b-135">CommonParameters</span></span>
<span data-ttu-id="a501b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a501b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a501b-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a501b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a501b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a501b-138">INPUTS</span></span>

### <span data-ttu-id="a501b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a501b-139">System.String</span></span>

### <span data-ttu-id="a501b-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="a501b-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="a501b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a501b-141">OUTPUTS</span></span>

### <span data-ttu-id="a501b-142">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a501b-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="a501b-143">Note</span><span class="sxs-lookup"><span data-stu-id="a501b-143">NOTES</span></span>

## <span data-ttu-id="a501b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a501b-144">RELATED LINKS</span></span>
