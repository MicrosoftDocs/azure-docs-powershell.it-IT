---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194415"
---
# <span data-ttu-id="e8d53-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="e8d53-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="e8d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8d53-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d53-103">Recupera i dettagli sui tipi di argomento supportati da Griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d53-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="e8d53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8d53-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8d53-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8d53-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d53-106">Recupera i dettagli dei tipi di argomento supportati da Griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d53-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="e8d53-107">Se si specifica il nome di un tipo di argomento, vengono restituiti dettagli sul tipo.</span><span class="sxs-lookup"><span data-stu-id="e8d53-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="e8d53-108">Se non si specificato il nome di un tipo di argomento, vengono restituiti dettagli su tutti i tipi di argomento.</span><span class="sxs-lookup"><span data-stu-id="e8d53-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="e8d53-109">Se si imposta IncludeEventTypes, nella risposta vengono incluse informazioni sui tipi di evento supportati da ogni tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="e8d53-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="e8d53-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8d53-110">EXAMPLES</span></span>

### <span data-ttu-id="e8d53-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8d53-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="e8d53-112">Ottiene un elenco dei tipi di argomento.</span><span class="sxs-lookup"><span data-stu-id="e8d53-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="e8d53-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e8d53-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="e8d53-114">Ottiene informazioni sul tipo di argomento StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="e8d53-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="e8d53-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e8d53-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="e8d53-116">Ottiene informazioni sul tipo di argomento StorageAccounts, inclusi i tipi di evento supportati da StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="e8d53-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="e8d53-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8d53-117">PARAMETERS</span></span>

### <span data-ttu-id="e8d53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d53-118">-DefaultProfile</span></span>
<span data-ttu-id="e8d53-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e8d53-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8d53-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="e8d53-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="e8d53-121">Se specificato, la risposta includerà i tipi di evento supportati da un tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="e8d53-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="e8d53-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8d53-122">-Name</span></span>
<span data-ttu-id="e8d53-123">Nome del tipo di argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e8d53-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="e8d53-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d53-124">CommonParameters</span></span>
<span data-ttu-id="e8d53-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d53-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d53-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8d53-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d53-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8d53-127">INPUTS</span></span>

### <span data-ttu-id="e8d53-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e8d53-128">System.String</span></span>

## <span data-ttu-id="e8d53-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8d53-129">OUTPUTS</span></span>

### <span data-ttu-id="e8d53-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="e8d53-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="e8d53-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="e8d53-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="e8d53-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8d53-132">NOTES</span></span>

## <span data-ttu-id="e8d53-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8d53-133">RELATED LINKS</span></span>
