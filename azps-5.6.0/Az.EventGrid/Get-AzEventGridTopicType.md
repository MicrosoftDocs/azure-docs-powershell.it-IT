---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 3a715e0c4c2540a0905035afabc15ef46caa32bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991296"
---
# <span data-ttu-id="34e57-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="34e57-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="34e57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e57-102">SYNOPSIS</span></span>
<span data-ttu-id="34e57-103">Recupera i dettagli sui tipi di argomento supportati da Griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="34e57-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="34e57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e57-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34e57-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34e57-105">DESCRIPTION</span></span>
<span data-ttu-id="34e57-106">Recupera i dettagli dei tipi di argomento supportati da Griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="34e57-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="34e57-107">Se si specifica il nome di un tipo di argomento, vengono restituiti dettagli su tale tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="34e57-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="34e57-108">Se non si specificato il nome di un tipo di argomento, vengono restituiti dettagli su tutti i tipi di argomento.</span><span class="sxs-lookup"><span data-stu-id="34e57-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="34e57-109">Se si imposta IncludeEventTypes, nella risposta vengono incluse informazioni sui tipi di evento supportati da ogni tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="34e57-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="34e57-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e57-110">EXAMPLES</span></span>

### <span data-ttu-id="34e57-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34e57-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="34e57-112">Ottiene un elenco dei tipi di argomento.</span><span class="sxs-lookup"><span data-stu-id="34e57-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="34e57-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="34e57-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="34e57-114">Ottiene informazioni sul tipo di argomento StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="34e57-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="34e57-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="34e57-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="34e57-116">Ottiene informazioni sul tipo di argomento StorageAccounts, inclusi i tipi di evento supportati da StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="34e57-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="34e57-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34e57-117">PARAMETERS</span></span>

### <span data-ttu-id="34e57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e57-118">-DefaultProfile</span></span>
<span data-ttu-id="34e57-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34e57-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34e57-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="34e57-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="34e57-121">Se specificato, la risposta includerà i tipi di evento supportati da un tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="34e57-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="34e57-122">-Name</span><span class="sxs-lookup"><span data-stu-id="34e57-122">-Name</span></span>
<span data-ttu-id="34e57-123">Nome del tipo di argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="34e57-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="34e57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e57-124">CommonParameters</span></span>
<span data-ttu-id="34e57-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e57-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34e57-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e57-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="34e57-127">INPUTS</span></span>

### <span data-ttu-id="34e57-128">System.String</span><span class="sxs-lookup"><span data-stu-id="34e57-128">System.String</span></span>

## <span data-ttu-id="34e57-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e57-129">OUTPUTS</span></span>

### <span data-ttu-id="34e57-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="34e57-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="34e57-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="34e57-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="34e57-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="34e57-132">NOTES</span></span>

## <span data-ttu-id="34e57-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e57-133">RELATED LINKS</span></span>
