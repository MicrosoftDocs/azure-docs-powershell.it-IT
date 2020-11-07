---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687260"
---
# <span data-ttu-id="29797-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="29797-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="29797-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29797-102">SYNOPSIS</span></span>
<span data-ttu-id="29797-103">Ottiene i contatti di sicurezza configurati in questo abbonamento</span><span class="sxs-lookup"><span data-stu-id="29797-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29797-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29797-104">SYNTAX</span></span>

### <span data-ttu-id="29797-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29797-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29797-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="29797-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29797-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29797-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29797-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29797-108">DESCRIPTION</span></span>
<span data-ttu-id="29797-109">Ottiene i contatti di sicurezza configurati in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29797-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="29797-110">Il contatto di sicurezza può ricevere notifiche sugli avvisi di sicurezza che si verificano nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29797-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="29797-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29797-111">EXAMPLES</span></span>

### <span data-ttu-id="29797-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29797-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="29797-113">Ottiene tutti i contatti di sicurezza configurati nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="29797-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="29797-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29797-114">PARAMETERS</span></span>

### <span data-ttu-id="29797-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29797-115">-DefaultProfile</span></span>
<span data-ttu-id="29797-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29797-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29797-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="29797-117">-Name</span></span>
<span data-ttu-id="29797-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="29797-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29797-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29797-119">-ResourceId</span></span>
<span data-ttu-id="29797-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="29797-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29797-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29797-121">CommonParameters</span></span>
<span data-ttu-id="29797-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29797-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29797-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29797-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29797-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29797-124">INPUTS</span></span>

### <span data-ttu-id="29797-125">System. String</span><span class="sxs-lookup"><span data-stu-id="29797-125">System.String</span></span>

## <span data-ttu-id="29797-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29797-126">OUTPUTS</span></span>

### <span data-ttu-id="29797-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="29797-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="29797-128">Note</span><span class="sxs-lookup"><span data-stu-id="29797-128">NOTES</span></span>

## <span data-ttu-id="29797-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29797-129">RELATED LINKS</span></span>
