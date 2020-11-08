---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: e115e5dc9537ace9275517c74057e5f99d80e006
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019556"
---
# <span data-ttu-id="fda91-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="fda91-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="fda91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fda91-102">SYNOPSIS</span></span>
<span data-ttu-id="fda91-103">Ottiene i contatti di sicurezza configurati in questo abbonamento</span><span class="sxs-lookup"><span data-stu-id="fda91-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="fda91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fda91-104">SYNTAX</span></span>

### <span data-ttu-id="fda91-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fda91-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fda91-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fda91-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fda91-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda91-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fda91-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fda91-108">DESCRIPTION</span></span>
<span data-ttu-id="fda91-109">Ottiene i contatti di sicurezza configurati in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fda91-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="fda91-110">Il contatto di sicurezza può ricevere notifiche sugli avvisi di sicurezza che si verificano nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fda91-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="fda91-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fda91-111">EXAMPLES</span></span>

### <span data-ttu-id="fda91-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fda91-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="fda91-113">Ottiene tutti i contatti di sicurezza configurati nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="fda91-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="fda91-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fda91-114">PARAMETERS</span></span>

### <span data-ttu-id="fda91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda91-115">-DefaultProfile</span></span>
<span data-ttu-id="fda91-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fda91-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda91-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fda91-117">-Name</span></span>
<span data-ttu-id="fda91-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="fda91-118">Resource name.</span></span>

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

### <span data-ttu-id="fda91-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda91-119">-ResourceId</span></span>
<span data-ttu-id="fda91-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fda91-120">Resource ID.</span></span>

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

### <span data-ttu-id="fda91-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda91-121">CommonParameters</span></span>
<span data-ttu-id="fda91-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda91-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda91-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda91-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda91-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fda91-124">INPUTS</span></span>

### <span data-ttu-id="fda91-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fda91-125">System.String</span></span>

## <span data-ttu-id="fda91-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fda91-126">OUTPUTS</span></span>

### <span data-ttu-id="fda91-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="fda91-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="fda91-128">Note</span><span class="sxs-lookup"><span data-stu-id="fda91-128">NOTES</span></span>

## <span data-ttu-id="fda91-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fda91-129">RELATED LINKS</span></span>
