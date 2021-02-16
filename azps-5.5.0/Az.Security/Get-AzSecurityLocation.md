---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189190"
---
# <span data-ttu-id="1c9bd-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="1c9bd-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="1c9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9bd-103">Ottiene la posizione in cui il Centro sicurezza e protezione di Azure salverà automaticamente i dati per la sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="1c9bd-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="1c9bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c9bd-104">SYNTAX</span></span>

### <span data-ttu-id="1c9bd-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c9bd-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9bd-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1c9bd-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c9bd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9bd-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c9bd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c9bd-108">DESCRIPTION</span></span>
<span data-ttu-id="1c9bd-109">Il Centro sicurezza di Azure deciderà automaticamente una posizione in cui salvare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="1c9bd-110">Usare questo cmdlet per individuare la posizione.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="1c9bd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c9bd-111">EXAMPLES</span></span>

### <span data-ttu-id="1c9bd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c9bd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="1c9bd-113">Ottiene la posizione in cui il Centro sicurezza di Azure salva i dati di sicurezza calcolati.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="1c9bd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c9bd-114">PARAMETERS</span></span>

### <span data-ttu-id="1c9bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9bd-115">-DefaultProfile</span></span>
<span data-ttu-id="1c9bd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9bd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1c9bd-117">-Name</span></span>
<span data-ttu-id="1c9bd-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-118">Resource name.</span></span>

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

### <span data-ttu-id="1c9bd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9bd-119">-ResourceId</span></span>
<span data-ttu-id="1c9bd-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-120">Resource ID.</span></span>

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

### <span data-ttu-id="1c9bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9bd-121">CommonParameters</span></span>
<span data-ttu-id="1c9bd-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9bd-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c9bd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9bd-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c9bd-124">INPUTS</span></span>

### <span data-ttu-id="1c9bd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1c9bd-125">System.String</span></span>

## <span data-ttu-id="1c9bd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c9bd-126">OUTPUTS</span></span>

### <span data-ttu-id="1c9bd-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="1c9bd-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="1c9bd-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c9bd-128">NOTES</span></span>

## <span data-ttu-id="1c9bd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c9bd-129">RELATED LINKS</span></span>
