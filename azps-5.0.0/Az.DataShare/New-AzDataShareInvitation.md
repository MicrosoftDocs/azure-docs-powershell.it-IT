---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297439"
---
# <span data-ttu-id="2dd58-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="2dd58-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="2dd58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dd58-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd58-103">Crea un invito per la condivisione.</span><span class="sxs-lookup"><span data-stu-id="2dd58-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="2dd58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dd58-104">SYNTAX</span></span>

### <span data-ttu-id="2dd58-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2dd58-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd58-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd58-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd58-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd58-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd58-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dd58-108">DESCRIPTION</span></span>
<span data-ttu-id="2dd58-109">Il cmdlet **New-AzDataShareInvitation** Invia un invito al consumer di destinazione con le informazioni sulla condivisione del provider.</span><span class="sxs-lookup"><span data-stu-id="2dd58-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="2dd58-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dd58-110">EXAMPLES</span></span>

### <span data-ttu-id="2dd58-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2dd58-111">Example 1</span></span>
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

<span data-ttu-id="2dd58-112">Questo comando crea un invito AdsInvitation per la condivisione di AdsShare e lo invia al messaggio di posta elettronica di destinazione adstest@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="2dd58-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="2dd58-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dd58-113">PARAMETERS</span></span>

### <span data-ttu-id="2dd58-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2dd58-114">-AccountName</span></span>
<span data-ttu-id="2dd58-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2dd58-115">Azure data share account name</span></span>

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

### <span data-ttu-id="2dd58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd58-116">-DefaultProfile</span></span>
<span data-ttu-id="2dd58-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd58-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dd58-118">-Name</span></span>
<span data-ttu-id="2dd58-119">Nome dell'invito della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2dd58-119">Azure data share invitation name</span></span>

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

### <span data-ttu-id="2dd58-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd58-120">-ResourceGroupName</span></span>
<span data-ttu-id="2dd58-121">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2dd58-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2dd58-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2dd58-122">-ShareName</span></span>
<span data-ttu-id="2dd58-123">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2dd58-123">Azure data share name</span></span>

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

### <span data-ttu-id="2dd58-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="2dd58-124">-TargetEmail</span></span>
<span data-ttu-id="2dd58-125">ID posta elettronica di destinazione</span><span class="sxs-lookup"><span data-stu-id="2dd58-125">Target email id</span></span>

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

### <span data-ttu-id="2dd58-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="2dd58-126">-TargetObjectId</span></span>
<span data-ttu-id="2dd58-127">ID oggetto di destinazione</span><span class="sxs-lookup"><span data-stu-id="2dd58-127">Target object id</span></span>

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

### <span data-ttu-id="2dd58-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="2dd58-128">-TargetTenantId</span></span>
<span data-ttu-id="2dd58-129">ID tenant di destinazione</span><span class="sxs-lookup"><span data-stu-id="2dd58-129">Target tenant id</span></span>

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

### <span data-ttu-id="2dd58-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2dd58-130">-Confirm</span></span>
<span data-ttu-id="2dd58-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd58-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd58-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd58-132">-WhatIf</span></span>
<span data-ttu-id="2dd58-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2dd58-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd58-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2dd58-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd58-135">CommonParameters</span></span>
<span data-ttu-id="2dd58-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd58-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dd58-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd58-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dd58-138">INPUTS</span></span>

### <span data-ttu-id="2dd58-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2dd58-139">None</span></span>

## <span data-ttu-id="2dd58-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dd58-140">OUTPUTS</span></span>

### <span data-ttu-id="2dd58-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="2dd58-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="2dd58-142">Note</span><span class="sxs-lookup"><span data-stu-id="2dd58-142">NOTES</span></span>

## <span data-ttu-id="2dd58-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dd58-143">RELATED LINKS</span></span>
