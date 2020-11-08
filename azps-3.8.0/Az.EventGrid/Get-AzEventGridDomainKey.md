---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: f4bc6e7b505f48fe335a5bbc19703032e9ecf06d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018669"
---
# <span data-ttu-id="c381f-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c381f-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="c381f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c381f-102">SYNOPSIS</span></span>
<span data-ttu-id="c381f-103">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="c381f-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="c381f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c381f-104">SYNTAX</span></span>

### <span data-ttu-id="c381f-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c381f-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c381f-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c381f-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c381f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c381f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c381f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c381f-108">DESCRIPTION</span></span>
<span data-ttu-id="c381f-109">Ottiene i tasti di scelta condivisi usati per pubblicare gli eventi in un dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="c381f-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="c381f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c381f-110">EXAMPLES</span></span>

### <span data-ttu-id="c381f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c381f-111">Example 1</span></span>

<span data-ttu-id="c381f-112">Ottiene i tasti di scelta condivisi del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c381f-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="c381f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c381f-113">Example 2</span></span>

<span data-ttu-id="c381f-114">Ottiene i tasti di scelta condivisi del dominio della griglia dell'evento \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c381f-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="c381f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c381f-115">PARAMETERS</span></span>

### <span data-ttu-id="c381f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c381f-116">-DefaultProfile</span></span>
<span data-ttu-id="c381f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c381f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c381f-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="c381f-118">-DomainObject</span></span>
<span data-ttu-id="c381f-119">Oggetto di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c381f-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="c381f-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="c381f-120">-DomainResourceId</span></span>
<span data-ttu-id="c381f-121">Identificatore delle risorse che rappresenta il dominio della griglia dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c381f-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="c381f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c381f-122">-Name</span></span>
<span data-ttu-id="c381f-123">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c381f-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c381f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c381f-124">-ResourceGroupName</span></span>
<span data-ttu-id="c381f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c381f-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c381f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c381f-126">CommonParameters</span></span>
<span data-ttu-id="c381f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c381f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c381f-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c381f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c381f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c381f-129">INPUTS</span></span>

### <span data-ttu-id="c381f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c381f-130">System.String</span></span>

### <span data-ttu-id="c381f-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="c381f-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="c381f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c381f-132">OUTPUTS</span></span>

### <span data-ttu-id="c381f-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c381f-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="c381f-134">Note</span><span class="sxs-lookup"><span data-stu-id="c381f-134">NOTES</span></span>

## <span data-ttu-id="c381f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c381f-135">RELATED LINKS</span></span>
