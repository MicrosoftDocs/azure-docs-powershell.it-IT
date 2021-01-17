---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335176"
---
# <span data-ttu-id="12ba0-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="12ba0-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="12ba0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="12ba0-103">Ottiene la posizione in cui Azure Security Center salverà automaticamente i dati per l'abbonamento specifico</span><span class="sxs-lookup"><span data-stu-id="12ba0-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="12ba0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ba0-104">SYNTAX</span></span>

### <span data-ttu-id="12ba0-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12ba0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ba0-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="12ba0-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ba0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ba0-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ba0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12ba0-108">DESCRIPTION</span></span>
<span data-ttu-id="12ba0-109">Azure Security Center deciderà automaticamente in un percorso per salvare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="12ba0-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="12ba0-110">Usa questo cmdlet per scoprire la posizione.</span><span class="sxs-lookup"><span data-stu-id="12ba0-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="12ba0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ba0-111">EXAMPLES</span></span>

### <span data-ttu-id="12ba0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12ba0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="12ba0-113">Ottiene la posizione in cui Azure Security Center Salva i dati di sicurezza calcolati.</span><span class="sxs-lookup"><span data-stu-id="12ba0-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="12ba0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12ba0-114">PARAMETERS</span></span>

### <span data-ttu-id="12ba0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ba0-115">-DefaultProfile</span></span>
<span data-ttu-id="12ba0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12ba0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ba0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="12ba0-117">-Name</span></span>
<span data-ttu-id="12ba0-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="12ba0-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ba0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ba0-119">-ResourceId</span></span>
<span data-ttu-id="12ba0-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="12ba0-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ba0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ba0-121">CommonParameters</span></span>
<span data-ttu-id="12ba0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ba0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ba0-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12ba0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ba0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12ba0-124">INPUTS</span></span>

### <span data-ttu-id="12ba0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="12ba0-125">System.String</span></span>

## <span data-ttu-id="12ba0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ba0-126">OUTPUTS</span></span>

### <span data-ttu-id="12ba0-127">Microsoft. Azure. Commands. Security. Models. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="12ba0-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="12ba0-128">Note</span><span class="sxs-lookup"><span data-stu-id="12ba0-128">NOTES</span></span>

## <span data-ttu-id="12ba0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ba0-129">RELATED LINKS</span></span>
