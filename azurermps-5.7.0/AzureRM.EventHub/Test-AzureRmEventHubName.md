---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514328"
---
# <span data-ttu-id="08dbf-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="08dbf-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="08dbf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="08dbf-103">Controlla la disponibilità del nome o dell'alias dello spazio dei nomi assegnato (nome configurazione DR)</span><span class="sxs-lookup"><span data-stu-id="08dbf-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08dbf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08dbf-104">SYNTAX</span></span>

### <span data-ttu-id="08dbf-105">NamespaceCheckNameAvailabilitySet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08dbf-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08dbf-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="08dbf-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08dbf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08dbf-107">DESCRIPTION</span></span>
<span data-ttu-id="08dbf-108">Il cmdlet **test-AzureRmEventhubName** verifica la disponibilità del nome dello spazio dei nomi o dell'alias (nome configurazione Dr)</span><span class="sxs-lookup"><span data-stu-id="08dbf-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="08dbf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08dbf-109">EXAMPLES</span></span>

### <span data-ttu-id="08dbf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08dbf-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="08dbf-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come vero</span><span class="sxs-lookup"><span data-stu-id="08dbf-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="08dbf-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="08dbf-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="08dbf-113">Restituisce lo stato della disponibilità del nome dello spazio dei nomi ' MyNameSapceName ' come falso con motivo</span><span class="sxs-lookup"><span data-stu-id="08dbf-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="08dbf-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="08dbf-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="08dbf-115">Restituisce lo stato della disponibilità del nome alias "aliasname" in spazio dei nomi "MyNameSapceName" come vero</span><span class="sxs-lookup"><span data-stu-id="08dbf-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="08dbf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08dbf-116">PARAMETERS</span></span>

### <span data-ttu-id="08dbf-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="08dbf-117">-AliasName</span></span>
<span data-ttu-id="08dbf-118">Nome configurazione DR-nome alias</span><span class="sxs-lookup"><span data-stu-id="08dbf-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08dbf-119">-DefaultProfile</span></span>
<span data-ttu-id="08dbf-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08dbf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08dbf-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08dbf-121">-Namespace</span></span>
<span data-ttu-id="08dbf-122">Nome dello spazio dei nomi Eventhub</span><span class="sxs-lookup"><span data-stu-id="08dbf-122">Eventhub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dbf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08dbf-123">-ResourceGroupName</span></span>
<span data-ttu-id="08dbf-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="08dbf-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dbf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08dbf-125">CommonParameters</span></span>
<span data-ttu-id="08dbf-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08dbf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="08dbf-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08dbf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08dbf-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08dbf-128">INPUTS</span></span>

### <span data-ttu-id="08dbf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="08dbf-129">System.String</span></span>


## <span data-ttu-id="08dbf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08dbf-130">OUTPUTS</span></span>

### <span data-ttu-id="08dbf-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="08dbf-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="08dbf-132">Note</span><span class="sxs-lookup"><span data-stu-id="08dbf-132">NOTES</span></span>

## <span data-ttu-id="08dbf-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08dbf-133">RELATED LINKS</span></span>
