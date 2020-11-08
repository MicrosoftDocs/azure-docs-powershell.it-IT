---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192903"
---
# <span data-ttu-id="f31a2-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="f31a2-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="f31a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f31a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f31a2-103">Creare un oggetto PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="f31a2-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="f31a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f31a2-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f31a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f31a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f31a2-106">Crea un oggetto PSHeaderAction per la creazione di un oggetto PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="f31a2-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="f31a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f31a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f31a2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f31a2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="f31a2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f31a2-109">PARAMETERS</span></span>

### <span data-ttu-id="f31a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31a2-110">-DefaultProfile</span></span>
<span data-ttu-id="f31a2-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f31a2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31a2-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="f31a2-112">-HeaderActionType</span></span>
<span data-ttu-id="f31a2-113">Tipo di manipolazione da applicare all'intestazione.</span><span class="sxs-lookup"><span data-stu-id="f31a2-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31a2-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="f31a2-114">-HeaderName</span></span>
<span data-ttu-id="f31a2-115">Nome dell'intestazione a cui verrà applicata l'azione.</span><span class="sxs-lookup"><span data-stu-id="f31a2-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31a2-116">-Valore</span><span class="sxs-lookup"><span data-stu-id="f31a2-116">-Value</span></span>
<span data-ttu-id="f31a2-117">Il valore per aggiornare il nome di intestazione indicato con.</span><span class="sxs-lookup"><span data-stu-id="f31a2-117">The value to update the given header name with.</span></span>
<span data-ttu-id="f31a2-118">Questo valore non viene usato se actionType è DELETE.</span><span class="sxs-lookup"><span data-stu-id="f31a2-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31a2-119">CommonParameters</span></span>
<span data-ttu-id="f31a2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31a2-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f31a2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31a2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f31a2-122">INPUTS</span></span>

### <span data-ttu-id="f31a2-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f31a2-123">None</span></span>

## <span data-ttu-id="f31a2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f31a2-124">OUTPUTS</span></span>

### <span data-ttu-id="f31a2-125">Microsoft. Azure. Commands. FrontDoor. Models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="f31a2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="f31a2-126">Note</span><span class="sxs-lookup"><span data-stu-id="f31a2-126">NOTES</span></span>

## <span data-ttu-id="f31a2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f31a2-127">RELATED LINKS</span></span>
