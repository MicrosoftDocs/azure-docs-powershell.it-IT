---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191604"
---
# <span data-ttu-id="8f942-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8f942-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="8f942-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f942-102">SYNOPSIS</span></span>
<span data-ttu-id="8f942-103">Crea un nuovo abbonamento a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="8f942-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="8f942-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f942-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f942-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f942-105">DESCRIPTION</span></span>
<span data-ttu-id="8f942-106">Il cmdlet **New-AzDataShareSubscription** crea un abbonamento a una condivisione nell'account di condivisione dati e nell'ID invito specificati.</span><span class="sxs-lookup"><span data-stu-id="8f942-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="8f942-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f942-107">EXAMPLES</span></span>

### <span data-ttu-id="8f942-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f942-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="8f942-109">Questo comando crea una nuova AdsShareSubscription di sottoscrizione di condivisione per invitaionId in WikiAds account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="8f942-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="8f942-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f942-110">PARAMETERS</span></span>

### <span data-ttu-id="8f942-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8f942-111">-AccountName</span></span>
<span data-ttu-id="8f942-112">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8f942-112">Azure data share account name</span></span>

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

### <span data-ttu-id="8f942-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f942-113">-DefaultProfile</span></span>
<span data-ttu-id="8f942-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f942-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f942-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="8f942-115">-InvitationId</span></span>
<span data-ttu-id="8f942-116">Condivisione dati di Azure invitationId</span><span class="sxs-lookup"><span data-stu-id="8f942-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="8f942-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f942-117">-Name</span></span>
<span data-ttu-id="8f942-118">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8f942-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8f942-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f942-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f942-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8f942-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8f942-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="8f942-121">-SourceShareLocation</span></span>
<span data-ttu-id="8f942-122">Posizione della condivisione dati in Azure</span><span class="sxs-lookup"><span data-stu-id="8f942-122">Azure data share location</span></span>

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

### <span data-ttu-id="8f942-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f942-123">-Confirm</span></span>
<span data-ttu-id="8f942-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f942-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f942-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f942-125">-WhatIf</span></span>
<span data-ttu-id="8f942-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f942-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f942-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f942-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f942-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f942-128">CommonParameters</span></span>
<span data-ttu-id="8f942-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f942-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f942-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f942-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f942-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f942-131">INPUTS</span></span>

### <span data-ttu-id="8f942-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8f942-132">None</span></span>

## <span data-ttu-id="8f942-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f942-133">OUTPUTS</span></span>

### <span data-ttu-id="8f942-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8f942-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8f942-135">Note</span><span class="sxs-lookup"><span data-stu-id="8f942-135">NOTES</span></span>

## <span data-ttu-id="8f942-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f942-136">RELATED LINKS</span></span>