---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297415"
---
# <span data-ttu-id="511e7-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="511e7-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="511e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="511e7-102">SYNOPSIS</span></span>
<span data-ttu-id="511e7-103">Rimuove un account DataShare</span><span class="sxs-lookup"><span data-stu-id="511e7-103">Removes a datashare account</span></span>

## <span data-ttu-id="511e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="511e7-104">SYNTAX</span></span>

### <span data-ttu-id="511e7-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="511e7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511e7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="511e7-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511e7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="511e7-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511e7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="511e7-108">DESCRIPTION</span></span>
<span data-ttu-id="511e7-109">Il cmdlet **Remove-AzDataShareAccount** rimuove un account DataShare.</span><span class="sxs-lookup"><span data-stu-id="511e7-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="511e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="511e7-110">EXAMPLES</span></span>

### <span data-ttu-id="511e7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="511e7-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="511e7-112">Questo comando rimuove l'account DataShare denominato WikiADS dal gruppo risorse denominato annunci.</span><span class="sxs-lookup"><span data-stu-id="511e7-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="511e7-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="511e7-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="511e7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="511e7-114">PARAMETERS</span></span>

### <span data-ttu-id="511e7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="511e7-115">-AsJob</span></span>
<span data-ttu-id="511e7-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="511e7-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="511e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511e7-117">-DefaultProfile</span></span>
<span data-ttu-id="511e7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="511e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="511e7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="511e7-119">-Force</span></span>
<span data-ttu-id="511e7-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="511e7-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="511e7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="511e7-121">-InputObject</span></span>
<span data-ttu-id="511e7-122">Oggetto account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="511e7-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="511e7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="511e7-123">-Name</span></span>
<span data-ttu-id="511e7-124">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="511e7-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="511e7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="511e7-125">-PassThru</span></span>
<span data-ttu-id="511e7-126">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="511e7-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="511e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="511e7-128">Nome del gruppo di risorse di Azure Data Share account.</span><span class="sxs-lookup"><span data-stu-id="511e7-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="511e7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="511e7-129">-ResourceId</span></span>
<span data-ttu-id="511e7-130">ID risorsa dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="511e7-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="511e7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="511e7-131">-Confirm</span></span>
<span data-ttu-id="511e7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511e7-133">-WhatIf</span></span>
<span data-ttu-id="511e7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="511e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511e7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="511e7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511e7-136">CommonParameters</span></span>
<span data-ttu-id="511e7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511e7-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="511e7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511e7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="511e7-139">INPUTS</span></span>

### <span data-ttu-id="511e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="511e7-140">System.String</span></span>

### <span data-ttu-id="511e7-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="511e7-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="511e7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="511e7-142">OUTPUTS</span></span>

### <span data-ttu-id="511e7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="511e7-143">System.Boolean</span></span>

## <span data-ttu-id="511e7-144">Note</span><span class="sxs-lookup"><span data-stu-id="511e7-144">NOTES</span></span>

## <span data-ttu-id="511e7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="511e7-145">RELATED LINKS</span></span>
