---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: a27989a1637443335389ba8b35bd90279a8976f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996727"
---
# <span data-ttu-id="fa265-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="fa265-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="fa265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa265-102">SYNOPSIS</span></span>
<span data-ttu-id="fa265-103">Crea un invito per la condivisione.</span><span class="sxs-lookup"><span data-stu-id="fa265-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="fa265-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa265-104">SYNTAX</span></span>

### <span data-ttu-id="fa265-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa265-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa265-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa265-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa265-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa265-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa265-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa265-108">DESCRIPTION</span></span>
<span data-ttu-id="fa265-109">Il cmdlet **New-AzDataShareInvitation** invia un invito al consumer di destinazione con informazioni sulla condivisione del provider.</span><span class="sxs-lookup"><span data-stu-id="fa265-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="fa265-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa265-110">EXAMPLES</span></span>

### <span data-ttu-id="fa265-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa265-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="fa265-112">Questo comando crea un invito AdsInvitation per condividere AdsShare e lo invia all'indirizzo di posta elettronica di adstest@microsoft.com destinazione.</span><span class="sxs-lookup"><span data-stu-id="fa265-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="fa265-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa265-113">PARAMETERS</span></span>

### <span data-ttu-id="fa265-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fa265-114">-AccountName</span></span>
<span data-ttu-id="fa265-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fa265-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa265-116">-DefaultProfile</span></span>
<span data-ttu-id="fa265-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa265-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa265-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fa265-118">-Name</span></span>
<span data-ttu-id="fa265-119">Nome invito per la condivisione di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fa265-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa265-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa265-121">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fa265-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fa265-122">-ShareName</span></span>
<span data-ttu-id="fa265-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fa265-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="fa265-124">-TargetEmail</span></span>
<span data-ttu-id="fa265-125">ID di posta elettronica di destinazione</span><span class="sxs-lookup"><span data-stu-id="fa265-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="fa265-126">-TargetObjectId</span></span>
<span data-ttu-id="fa265-127">ID oggetto di destinazione</span><span class="sxs-lookup"><span data-stu-id="fa265-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="fa265-128">-TargetTenantId</span></span>
<span data-ttu-id="fa265-129">ID tenant di destinazione</span><span class="sxs-lookup"><span data-stu-id="fa265-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa265-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa265-130">-Confirm</span></span>
<span data-ttu-id="fa265-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa265-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa265-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa265-132">-WhatIf</span></span>
<span data-ttu-id="fa265-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa265-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa265-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa265-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa265-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa265-135">CommonParameters</span></span>
<span data-ttu-id="fa265-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa265-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa265-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa265-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa265-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa265-138">INPUTS</span></span>

### <span data-ttu-id="fa265-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fa265-139">None</span></span>

## <span data-ttu-id="fa265-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa265-140">OUTPUTS</span></span>

### <span data-ttu-id="fa265-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="fa265-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="fa265-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa265-142">NOTES</span></span>

## <span data-ttu-id="fa265-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa265-143">RELATED LINKS</span></span>
