---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996713"
---
# <span data-ttu-id="04307-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="04307-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="04307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04307-102">SYNOPSIS</span></span>
<span data-ttu-id="04307-103">Crea una nuova sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="04307-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="04307-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04307-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04307-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04307-105">DESCRIPTION</span></span>
<span data-ttu-id="04307-106">Il cmdlet **New-AzDataShareSubscription** crea una sottoscrizione di condivisione nell'account di condivisione dati specificato e nell'ID invito.</span><span class="sxs-lookup"><span data-stu-id="04307-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="04307-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04307-107">EXAMPLES</span></span>

### <span data-ttu-id="04307-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04307-108">Example 1</span></span>
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

<span data-ttu-id="04307-109">Questo comando crea una nuova sottoscrizione di condivisione AdsShareSubscription per invitaionId nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="04307-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="04307-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04307-110">PARAMETERS</span></span>

### <span data-ttu-id="04307-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04307-111">-AccountName</span></span>
<span data-ttu-id="04307-112">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="04307-112">Azure data share account name</span></span>

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

### <span data-ttu-id="04307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04307-113">-DefaultProfile</span></span>
<span data-ttu-id="04307-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04307-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04307-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="04307-115">-InvitationId</span></span>
<span data-ttu-id="04307-116">InvitationId per la condivisione di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="04307-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="04307-117">-Name</span><span class="sxs-lookup"><span data-stu-id="04307-117">-Name</span></span>
<span data-ttu-id="04307-118">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="04307-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="04307-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04307-119">-ResourceGroupName</span></span>
<span data-ttu-id="04307-120">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="04307-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="04307-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="04307-121">-SourceShareLocation</span></span>
<span data-ttu-id="04307-122">Posizione di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="04307-122">Azure data share location</span></span>

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

### <span data-ttu-id="04307-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04307-123">-Confirm</span></span>
<span data-ttu-id="04307-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04307-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04307-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04307-125">-WhatIf</span></span>
<span data-ttu-id="04307-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04307-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04307-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04307-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04307-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04307-128">CommonParameters</span></span>
<span data-ttu-id="04307-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04307-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04307-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04307-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04307-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="04307-131">INPUTS</span></span>

### <span data-ttu-id="04307-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="04307-132">None</span></span>

## <span data-ttu-id="04307-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04307-133">OUTPUTS</span></span>

### <span data-ttu-id="04307-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="04307-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="04307-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="04307-135">NOTES</span></span>

## <span data-ttu-id="04307-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04307-136">RELATED LINKS</span></span>
