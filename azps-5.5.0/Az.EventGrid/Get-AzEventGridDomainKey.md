---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209602"
---
# <span data-ttu-id="85783-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="85783-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="85783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85783-102">SYNOPSIS</span></span>
<span data-ttu-id="85783-103">Ottiene le chiavi di accesso condivise usate per pubblicare eventi in un dominio Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="85783-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="85783-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85783-104">SYNTAX</span></span>

### <span data-ttu-id="85783-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85783-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85783-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85783-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85783-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="85783-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85783-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85783-108">DESCRIPTION</span></span>
<span data-ttu-id="85783-109">Ottiene le chiavi di accesso condivise usate per pubblicare eventi in un dominio Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="85783-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="85783-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85783-110">EXAMPLES</span></span>

### <span data-ttu-id="85783-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85783-111">Example 1</span></span>

<span data-ttu-id="85783-112">Ottiene le chiavi di accesso condivise del dominio griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="85783-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="85783-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="85783-113">Example 2</span></span>

<span data-ttu-id="85783-114">Ottiene le chiavi di accesso condivise del dominio griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="85783-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="85783-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85783-115">PARAMETERS</span></span>

### <span data-ttu-id="85783-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85783-116">-DefaultProfile</span></span>
<span data-ttu-id="85783-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85783-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85783-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="85783-118">-DomainObject</span></span>
<span data-ttu-id="85783-119">Oggetto Dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="85783-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="85783-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="85783-120">-DomainResourceId</span></span>
<span data-ttu-id="85783-121">Identificatore di risorsa che rappresenta il dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="85783-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="85783-122">-Name</span><span class="sxs-lookup"><span data-stu-id="85783-122">-Name</span></span>
<span data-ttu-id="85783-123">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="85783-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="85783-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85783-124">-ResourceGroupName</span></span>
<span data-ttu-id="85783-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85783-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="85783-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85783-126">CommonParameters</span></span>
<span data-ttu-id="85783-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85783-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85783-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85783-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85783-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="85783-129">INPUTS</span></span>

### <span data-ttu-id="85783-130">System.String</span><span class="sxs-lookup"><span data-stu-id="85783-130">System.String</span></span>

### <span data-ttu-id="85783-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="85783-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="85783-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85783-132">OUTPUTS</span></span>

### <span data-ttu-id="85783-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="85783-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="85783-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="85783-134">NOTES</span></span>

## <span data-ttu-id="85783-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85783-135">RELATED LINKS</span></span>
