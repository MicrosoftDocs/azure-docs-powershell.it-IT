---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: a00edef30c327e9bce4e2fa008dad373a2e6367d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979341"
---
# <span data-ttu-id="a2c73-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a2c73-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="a2c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c73-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c73-103">Recupera i contatti di sicurezza configurati in questo abbonamento</span><span class="sxs-lookup"><span data-stu-id="a2c73-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="a2c73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2c73-104">SYNTAX</span></span>

### <span data-ttu-id="a2c73-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2c73-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c73-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a2c73-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c73-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c73-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c73-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2c73-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c73-109">Recupera i contatti di sicurezza configurati in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a2c73-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="a2c73-110">Il contatto di sicurezza può ricevere notifiche sugli avvisi di sicurezza che vengono visualizzati nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a2c73-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="a2c73-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2c73-111">EXAMPLES</span></span>

### <span data-ttu-id="a2c73-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2c73-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a2c73-113">Recupera tutti i contatti di sicurezza configurati nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="a2c73-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="a2c73-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c73-114">PARAMETERS</span></span>

### <span data-ttu-id="a2c73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c73-115">-DefaultProfile</span></span>
<span data-ttu-id="a2c73-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c73-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a2c73-117">-Name</span></span>
<span data-ttu-id="a2c73-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2c73-118">Resource name.</span></span>

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

### <span data-ttu-id="a2c73-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c73-119">-ResourceId</span></span>
<span data-ttu-id="a2c73-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2c73-120">Resource ID.</span></span>

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

### <span data-ttu-id="a2c73-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c73-121">CommonParameters</span></span>
<span data-ttu-id="a2c73-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c73-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c73-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2c73-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c73-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2c73-124">INPUTS</span></span>

### <span data-ttu-id="a2c73-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c73-125">System.String</span></span>

## <span data-ttu-id="a2c73-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2c73-126">OUTPUTS</span></span>

### <span data-ttu-id="a2c73-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a2c73-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a2c73-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2c73-128">NOTES</span></span>

## <span data-ttu-id="a2c73-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2c73-129">RELATED LINKS</span></span>
