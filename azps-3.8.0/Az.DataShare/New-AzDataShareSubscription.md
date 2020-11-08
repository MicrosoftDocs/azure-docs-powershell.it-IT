---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 01cff184a2db4364536d4088103380f3f28b47a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019787"
---
# <span data-ttu-id="b7729-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b7729-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="b7729-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7729-102">SYNOPSIS</span></span>
<span data-ttu-id="b7729-103">Crea un nuovo abbonamento a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="b7729-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="b7729-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7729-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7729-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7729-105">DESCRIPTION</span></span>
<span data-ttu-id="b7729-106">Il cmdlet **New-AzDataShareSubscription** crea un abbonamento a una condivisione nell'account di condivisione dati e nell'ID invito specificati.</span><span class="sxs-lookup"><span data-stu-id="b7729-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="b7729-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7729-107">EXAMPLES</span></span>

### <span data-ttu-id="b7729-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7729-108">Example 1</span></span>
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

<span data-ttu-id="b7729-109">Questo comando crea una nuova AdsShareSubscription di sottoscrizione di condivisione per invitaionId in WikiAds account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="b7729-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="b7729-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7729-110">PARAMETERS</span></span>

### <span data-ttu-id="b7729-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7729-111">-AccountName</span></span>
<span data-ttu-id="b7729-112">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b7729-112">Azure data share account name</span></span>

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

### <span data-ttu-id="b7729-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7729-113">-DefaultProfile</span></span>
<span data-ttu-id="b7729-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7729-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7729-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="b7729-115">-InvitationId</span></span>
<span data-ttu-id="b7729-116">Condivisione dati di Azure invitationId</span><span class="sxs-lookup"><span data-stu-id="b7729-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="b7729-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7729-117">-Name</span></span>
<span data-ttu-id="b7729-118">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b7729-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b7729-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7729-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7729-120">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b7729-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b7729-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7729-121">-Confirm</span></span>
<span data-ttu-id="b7729-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7729-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7729-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7729-123">-WhatIf</span></span>
<span data-ttu-id="b7729-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7729-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7729-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7729-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7729-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7729-126">CommonParameters</span></span>
<span data-ttu-id="b7729-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7729-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7729-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7729-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7729-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7729-129">INPUTS</span></span>

### <span data-ttu-id="b7729-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7729-130">None</span></span>

## <span data-ttu-id="b7729-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7729-131">OUTPUTS</span></span>

### <span data-ttu-id="b7729-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="b7729-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="b7729-133">Note</span><span class="sxs-lookup"><span data-stu-id="b7729-133">NOTES</span></span>

## <span data-ttu-id="b7729-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7729-134">RELATED LINKS</span></span>
