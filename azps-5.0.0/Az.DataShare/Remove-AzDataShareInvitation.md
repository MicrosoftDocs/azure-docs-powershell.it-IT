---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297402"
---
# <span data-ttu-id="4a454-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="4a454-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="4a454-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a454-102">SYNOPSIS</span></span>
<span data-ttu-id="4a454-103">Rimuove un invito</span><span class="sxs-lookup"><span data-stu-id="4a454-103">removes an invitation</span></span>

## <span data-ttu-id="4a454-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a454-104">SYNTAX</span></span>

### <span data-ttu-id="4a454-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a454-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a454-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a454-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a454-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a454-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a454-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a454-108">DESCRIPTION</span></span>
<span data-ttu-id="4a454-109">Il cmdlet **Remove-AzDataShareInvitation** rimuove un invito DataShare.</span><span class="sxs-lookup"><span data-stu-id="4a454-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="4a454-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a454-110">EXAMPLES</span></span>

### <span data-ttu-id="4a454-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a454-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4a454-112">Questo comando rimuove un invito denominato ADSInvite da Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="4a454-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="4a454-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a454-113">PARAMETERS</span></span>

### <span data-ttu-id="4a454-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a454-114">-AccountName</span></span>
<span data-ttu-id="4a454-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4a454-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a454-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a454-116">-DefaultProfile</span></span>
<span data-ttu-id="4a454-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a454-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a454-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a454-118">-InputObject</span></span>
<span data-ttu-id="4a454-119">Oggetto invito di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4a454-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a454-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a454-120">-Name</span></span>
<span data-ttu-id="4a454-121">Nome dell'invito della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4a454-121">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a454-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a454-122">-PassThru</span></span>
<span data-ttu-id="4a454-123">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="4a454-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="4a454-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a454-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a454-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4a454-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a454-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a454-126">-ResourceId</span></span>
<span data-ttu-id="4a454-127">ID risorsa dell'invito di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="4a454-127">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a454-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4a454-128">-ShareName</span></span>
<span data-ttu-id="4a454-129">Nome della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a454-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a454-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a454-130">-Confirm</span></span>
<span data-ttu-id="4a454-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a454-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a454-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a454-132">-WhatIf</span></span>
<span data-ttu-id="4a454-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a454-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a454-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a454-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a454-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a454-135">CommonParameters</span></span>
<span data-ttu-id="4a454-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a454-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a454-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a454-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a454-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a454-138">INPUTS</span></span>

### <span data-ttu-id="4a454-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4a454-139">System.String</span></span>

### <span data-ttu-id="4a454-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="4a454-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="4a454-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a454-141">OUTPUTS</span></span>

### <span data-ttu-id="4a454-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a454-142">System.Boolean</span></span>

## <span data-ttu-id="4a454-143">Note</span><span class="sxs-lookup"><span data-stu-id="4a454-143">NOTES</span></span>

## <span data-ttu-id="4a454-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a454-144">RELATED LINKS</span></span>
