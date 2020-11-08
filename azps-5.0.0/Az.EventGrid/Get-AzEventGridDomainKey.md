---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193435"
---
# <span data-ttu-id="a9bc5-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a9bc5-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="a9bc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bc5-103">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="a9bc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9bc5-104">SYNTAX</span></span>

### <span data-ttu-id="a9bc5-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9bc5-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9bc5-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bc5-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9bc5-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9bc5-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9bc5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9bc5-108">DESCRIPTION</span></span>
<span data-ttu-id="a9bc5-109">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="a9bc5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9bc5-110">EXAMPLES</span></span>

### <span data-ttu-id="a9bc5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9bc5-111">Example 1</span></span>

<span data-ttu-id="a9bc5-112">Ottiene i tasti di scelta condivisi del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a9bc5-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="a9bc5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a9bc5-113">Example 2</span></span>

<span data-ttu-id="a9bc5-114">Ottiene i tasti di scelta condivisi del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a9bc5-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="a9bc5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9bc5-115">PARAMETERS</span></span>

### <span data-ttu-id="a9bc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bc5-116">-DefaultProfile</span></span>
<span data-ttu-id="a9bc5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9bc5-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="a9bc5-118">-DomainObject</span></span>
<span data-ttu-id="a9bc5-119">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a9bc5-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="a9bc5-120">-DomainResourceId</span></span>
<span data-ttu-id="a9bc5-121">Identificatore delle risorse che rappresenta il dominio della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="a9bc5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9bc5-122">-Name</span></span>
<span data-ttu-id="a9bc5-123">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9bc5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9bc5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9bc5-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9bc5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bc5-126">CommonParameters</span></span>
<span data-ttu-id="a9bc5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bc5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bc5-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9bc5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bc5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9bc5-129">INPUTS</span></span>

### <span data-ttu-id="a9bc5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a9bc5-130">System.String</span></span>

### <span data-ttu-id="a9bc5-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="a9bc5-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="a9bc5-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9bc5-132">OUTPUTS</span></span>

### <span data-ttu-id="a9bc5-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a9bc5-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="a9bc5-134">Note</span><span class="sxs-lookup"><span data-stu-id="a9bc5-134">NOTES</span></span>

## <span data-ttu-id="a9bc5-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9bc5-135">RELATED LINKS</span></span>
