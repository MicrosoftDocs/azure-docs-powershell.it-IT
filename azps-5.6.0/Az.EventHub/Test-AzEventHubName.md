---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 6620579ad49143dc715fc62f23d305e2efd3d5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007886"
---
# <span data-ttu-id="e4b90-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="e4b90-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="e4b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4b90-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b90-103">Controlla la disponibilità del nome o alias namespace specificato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="e4b90-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="e4b90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4b90-104">SYNTAX</span></span>

### <span data-ttu-id="e4b90-105">NamespaceCheckNameAvailabilitySet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4b90-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4b90-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e4b90-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4b90-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4b90-107">DESCRIPTION</span></span>
<span data-ttu-id="e4b90-108">Il **cmdlet Test-AzEventhubName** controlla la disponibilità del nome o alias NameSpace (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="e4b90-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="e4b90-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4b90-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b90-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4b90-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="e4b90-111">Restituisce lo stato in base alla disponibilità dello spazio dei nomi 'NomeSapceName' come True, se disponibile</span><span class="sxs-lookup"><span data-stu-id="e4b90-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="e4b90-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e4b90-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="e4b90-113">Restituisce lo stato in base alla disponibilità dello spazio dei nomi 'NomeSapceName' come Falso con motivo</span><span class="sxs-lookup"><span data-stu-id="e4b90-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="e4b90-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e4b90-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="e4b90-115">Restituisce lo stato in base alla disponibilità del nome alias 'myAliasName' per lo spazio dei nomi 'MyNameSapceName' come True, se disponibile</span><span class="sxs-lookup"><span data-stu-id="e4b90-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="e4b90-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4b90-116">PARAMETERS</span></span>

### <span data-ttu-id="e4b90-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e4b90-117">-AliasName</span></span>
<span data-ttu-id="e4b90-118">DR Configuration Name - Alias Name</span><span class="sxs-lookup"><span data-stu-id="e4b90-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="e4b90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b90-119">-DefaultProfile</span></span>
<span data-ttu-id="e4b90-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b90-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4b90-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4b90-121">-Namespace</span></span>
<span data-ttu-id="e4b90-122">Nome spazio dei nomi di Eventhub</span><span class="sxs-lookup"><span data-stu-id="e4b90-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="e4b90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b90-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4b90-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e4b90-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e4b90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b90-125">CommonParameters</span></span>
<span data-ttu-id="e4b90-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b90-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b90-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b90-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4b90-128">INPUTS</span></span>

### <span data-ttu-id="e4b90-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e4b90-129">System.String</span></span>

## <span data-ttu-id="e4b90-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4b90-130">OUTPUTS</span></span>

### <span data-ttu-id="e4b90-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="e4b90-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="e4b90-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4b90-132">NOTES</span></span>

## <span data-ttu-id="e4b90-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4b90-133">RELATED LINKS</span></span>
