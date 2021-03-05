---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: a211e3857cd81a5dd057795fb9e2956d60cbae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984673"
---
# <span data-ttu-id="7fb6a-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7fb6a-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="7fb6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb6a-103">Ottiene le chiavi di accesso condivise usate per pubblicare eventi in un dominio Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="7fb6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fb6a-104">SYNTAX</span></span>

### <span data-ttu-id="7fb6a-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fb6a-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb6a-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fb6a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb6a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb6a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7fb6a-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb6a-109">Ottiene le chiavi di accesso condivise usate per pubblicare eventi in un dominio Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="7fb6a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fb6a-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb6a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fb6a-111">Example 1</span></span>

<span data-ttu-id="7fb6a-112">Ottiene le chiavi di accesso condivise del dominio griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="7fb6a-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="7fb6a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7fb6a-113">Example 2</span></span>

<span data-ttu-id="7fb6a-114">Ottiene le chiavi di accesso condivise del dominio griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="7fb6a-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="7fb6a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fb6a-115">PARAMETERS</span></span>

### <span data-ttu-id="7fb6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb6a-116">-DefaultProfile</span></span>
<span data-ttu-id="7fb6a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb6a-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="7fb6a-118">-DomainObject</span></span>
<span data-ttu-id="7fb6a-119">Oggetto Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="7fb6a-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="7fb6a-120">-DomainResourceId</span></span>
<span data-ttu-id="7fb6a-121">Identificatore di risorsa che rappresenta il dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="7fb6a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7fb6a-122">-Name</span></span>
<span data-ttu-id="7fb6a-123">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="7fb6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fb6a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fb6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb6a-126">CommonParameters</span></span>
<span data-ttu-id="7fb6a-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb6a-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb6a-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="7fb6a-129">INPUTS</span></span>

### <span data-ttu-id="7fb6a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7fb6a-130">System.String</span></span>

### <span data-ttu-id="7fb6a-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="7fb6a-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="7fb6a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fb6a-132">OUTPUTS</span></span>

### <span data-ttu-id="7fb6a-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7fb6a-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="7fb6a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="7fb6a-134">NOTES</span></span>

## <span data-ttu-id="7fb6a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fb6a-135">RELATED LINKS</span></span>
