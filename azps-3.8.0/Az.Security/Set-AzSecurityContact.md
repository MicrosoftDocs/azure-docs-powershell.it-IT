---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: c6351fb39158f7389c0f491a813890373df82cc1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021730"
---
# <span data-ttu-id="bc7cd-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="bc7cd-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="bc7cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7cd-103">Aggiorna un contatto di sicurezza per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="bc7cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc7cd-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc7cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="bc7cd-106">Aggiorna un contatto di sicurezza per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="bc7cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc7cd-107">EXAMPLES</span></span>

### <span data-ttu-id="bc7cd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc7cd-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="bc7cd-109">Aggiorna un contatto di sicurezza per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="bc7cd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc7cd-110">PARAMETERS</span></span>

### <span data-ttu-id="bc7cd-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="bc7cd-111">-AlertAdmin</span></span>
<span data-ttu-id="bc7cd-112">Avvisi per gli amministratori.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7cd-113">-DefaultProfile</span></span>
<span data-ttu-id="bc7cd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc7cd-115">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="bc7cd-115">-Email</span></span>
<span data-ttu-id="bc7cd-116">Posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-116">E-Mail.</span></span>

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

### <span data-ttu-id="bc7cd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc7cd-117">-Name</span></span>
<span data-ttu-id="bc7cd-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-118">Resource name.</span></span>

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

### <span data-ttu-id="bc7cd-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="bc7cd-119">-NotifyOnAlert</span></span>
<span data-ttu-id="bc7cd-120">Notifiche di avviso.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7cd-121">-Telefono</span><span class="sxs-lookup"><span data-stu-id="bc7cd-121">-Phone</span></span>
<span data-ttu-id="bc7cd-122">Telefono.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-122">Phone.</span></span>

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

### <span data-ttu-id="bc7cd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc7cd-123">-Confirm</span></span>
<span data-ttu-id="bc7cd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7cd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc7cd-125">-WhatIf</span></span>
<span data-ttu-id="bc7cd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc7cd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7cd-128">CommonParameters</span></span>
<span data-ttu-id="bc7cd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc7cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7cd-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc7cd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7cd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc7cd-131">INPUTS</span></span>

### <span data-ttu-id="bc7cd-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bc7cd-132">None</span></span>

## <span data-ttu-id="bc7cd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc7cd-133">OUTPUTS</span></span>

### <span data-ttu-id="bc7cd-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="bc7cd-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="bc7cd-135">Note</span><span class="sxs-lookup"><span data-stu-id="bc7cd-135">NOTES</span></span>

## <span data-ttu-id="bc7cd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc7cd-136">RELATED LINKS</span></span>
