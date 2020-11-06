---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520095"
---
# <span data-ttu-id="4edaf-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="4edaf-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="4edaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4edaf-102">SYNOPSIS</span></span>
<span data-ttu-id="4edaf-103">Ottiene i dettagli relativi ai tipi di argomenti supportati dalla griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="4edaf-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4edaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4edaf-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4edaf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4edaf-105">DESCRIPTION</span></span>
<span data-ttu-id="4edaf-106">Ottiene i dettagli dei tipi di argomenti supportati dalla griglia di eventi Azure.</span><span class="sxs-lookup"><span data-stu-id="4edaf-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="4edaf-107">Se viene specificato un nome tipo di argomento, vengono restituiti i dettagli relativi al tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="4edaf-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="4edaf-108">Se non si specifica un nome di tipo di argomento, vengono restituiti i dettagli su tutti i tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="4edaf-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="4edaf-109">Se IncludeEventTypes è specificato, nella risposta vengono incluse informazioni sui tipi di evento supportati da ogni tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="4edaf-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="4edaf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4edaf-110">EXAMPLES</span></span>

### <span data-ttu-id="4edaf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4edaf-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="4edaf-112">Ottiene un elenco dei tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="4edaf-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="4edaf-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4edaf-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="4edaf-114">Ottiene le informazioni sul tipo di argomento StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="4edaf-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="4edaf-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4edaf-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="4edaf-116">Ottiene le informazioni sul tipo di argomento StorageAccounts, inclusi i tipi di evento supportati da StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="4edaf-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="4edaf-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4edaf-117">PARAMETERS</span></span>

### <span data-ttu-id="4edaf-118">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="4edaf-118">-IncludeEventTypeData</span></span>
<span data-ttu-id="4edaf-119">Se specificato, la risposta includerà i tipi di evento supportati da un tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="4edaf-119">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="4edaf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4edaf-120">-Name</span></span>
<span data-ttu-id="4edaf-121">Nome tipo argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="4edaf-121">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4edaf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4edaf-122">-DefaultProfile</span></span>
<span data-ttu-id="4edaf-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4edaf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4edaf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4edaf-124">CommonParameters</span></span>
<span data-ttu-id="4edaf-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4edaf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4edaf-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4edaf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4edaf-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4edaf-127">INPUTS</span></span>

### <span data-ttu-id="4edaf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4edaf-128">System.String</span></span>
<span data-ttu-id="4edaf-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4edaf-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4edaf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4edaf-130">OUTPUTS</span></span>

### <span data-ttu-id="4edaf-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4edaf-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4edaf-132">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="4edaf-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="4edaf-133">Note</span><span class="sxs-lookup"><span data-stu-id="4edaf-133">NOTES</span></span>

## <span data-ttu-id="4edaf-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4edaf-134">RELATED LINKS</span></span>

