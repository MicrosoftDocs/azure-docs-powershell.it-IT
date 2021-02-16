---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204075"
---
# <span data-ttu-id="d76fd-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="d76fd-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="d76fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d76fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d76fd-103">Creare l'oggetto PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="d76fd-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="d76fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d76fd-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d76fd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d76fd-105">DESCRIPTION</span></span>
<span data-ttu-id="d76fd-106">Crea l'oggetto PSHeaderAction per la creazione dell'oggetto PSRulesActionAction.</span><span class="sxs-lookup"><span data-stu-id="d76fd-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="d76fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d76fd-107">EXAMPLES</span></span>

### <span data-ttu-id="d76fd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d76fd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="d76fd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d76fd-109">PARAMETERS</span></span>

### <span data-ttu-id="d76fd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76fd-110">-DefaultProfile</span></span>
<span data-ttu-id="d76fd-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d76fd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76fd-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="d76fd-112">-HeaderActionType</span></span>
<span data-ttu-id="d76fd-113">Tipo di modifica da applicare all'intestazione.</span><span class="sxs-lookup"><span data-stu-id="d76fd-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="d76fd-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="d76fd-114">-HeaderName</span></span>
<span data-ttu-id="d76fd-115">Nome dell'intestazione a cui verrà applicata questa azione.</span><span class="sxs-lookup"><span data-stu-id="d76fd-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="d76fd-116">-Value</span><span class="sxs-lookup"><span data-stu-id="d76fd-116">-Value</span></span>
<span data-ttu-id="d76fd-117">Valore con cui aggiornare il nome di intestazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d76fd-117">The value to update the given header name with.</span></span>
<span data-ttu-id="d76fd-118">Questo valore non viene usato se actionType è Delete.</span><span class="sxs-lookup"><span data-stu-id="d76fd-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="d76fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76fd-119">CommonParameters</span></span>
<span data-ttu-id="d76fd-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76fd-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d76fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76fd-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d76fd-122">INPUTS</span></span>

### <span data-ttu-id="d76fd-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d76fd-123">None</span></span>

## <span data-ttu-id="d76fd-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d76fd-124">OUTPUTS</span></span>

### <span data-ttu-id="d76fd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="d76fd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="d76fd-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d76fd-126">NOTES</span></span>

## <span data-ttu-id="d76fd-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d76fd-127">RELATED LINKS</span></span>
