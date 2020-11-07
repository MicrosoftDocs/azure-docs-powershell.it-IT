---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864461"
---
# <span data-ttu-id="b6476-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="b6476-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="b6476-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6476-102">SYNOPSIS</span></span>
<span data-ttu-id="b6476-103">Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="b6476-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="b6476-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6476-104">SYNTAX</span></span>

### <span data-ttu-id="b6476-105">NamespaceCheckNameAvailabilitySet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6476-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6476-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b6476-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6476-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6476-107">DESCRIPTION</span></span>
<span data-ttu-id="b6476-108">Il cmdlet **test-AzEventhubName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)</span><span class="sxs-lookup"><span data-stu-id="b6476-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="b6476-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6476-109">EXAMPLES</span></span>

### <span data-ttu-id="b6476-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6476-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="b6476-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero se disponibile</span><span class="sxs-lookup"><span data-stu-id="b6476-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="b6476-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b6476-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="b6476-113">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo</span><span class="sxs-lookup"><span data-stu-id="b6476-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="b6476-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b6476-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="b6476-115">Restituisce lo stato della disponibilità del nome alias ' aliasname ' per lo spazio dei nomi ' MyNameSapceName ' come vero se disponibile</span><span class="sxs-lookup"><span data-stu-id="b6476-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="b6476-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6476-116">PARAMETERS</span></span>

### <span data-ttu-id="b6476-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="b6476-117">-AliasName</span></span>
<span data-ttu-id="b6476-118">Nome configurazione DR-nome alias</span><span class="sxs-lookup"><span data-stu-id="b6476-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6476-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6476-119">-DefaultProfile</span></span>
<span data-ttu-id="b6476-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6476-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6476-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6476-121">-Namespace</span></span>
<span data-ttu-id="b6476-122">Nome dello spazio dei nomi Eventhub</span><span class="sxs-lookup"><span data-stu-id="b6476-122">Eventhub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6476-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6476-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6476-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b6476-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6476-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6476-125">CommonParameters</span></span>
<span data-ttu-id="b6476-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6476-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6476-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6476-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6476-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6476-128">INPUTS</span></span>

### <span data-ttu-id="b6476-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b6476-129">System.String</span></span>

## <span data-ttu-id="b6476-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6476-130">OUTPUTS</span></span>

### <span data-ttu-id="b6476-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="b6476-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="b6476-132">Note</span><span class="sxs-lookup"><span data-stu-id="b6476-132">NOTES</span></span>

## <span data-ttu-id="b6476-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6476-133">RELATED LINKS</span></span>
