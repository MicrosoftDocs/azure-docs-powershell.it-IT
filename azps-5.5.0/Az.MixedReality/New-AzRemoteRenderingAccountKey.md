---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180206"
---
# <span data-ttu-id="bb47b-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="bb47b-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="bb47b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb47b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb47b-103">Rigenerare la chiave dell'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="bb47b-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="bb47b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb47b-104">SYNTAX</span></span>

### <span data-ttu-id="bb47b-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb47b-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb47b-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb47b-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb47b-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb47b-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb47b-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb47b-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb47b-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb47b-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb47b-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb47b-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb47b-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb47b-111">DESCRIPTION</span></span>
<span data-ttu-id="bb47b-112">Rigenerare la chiave primaria o la chiave secondaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="bb47b-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="bb47b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb47b-113">EXAMPLES</span></span>

### <span data-ttu-id="bb47b-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb47b-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="bb47b-115">Rigenerare la chiave secondaria dell'account di rendering remoto "example" nel gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="bb47b-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="bb47b-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bb47b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="bb47b-117">Rigenerare la chiave secondaria dell'account di rendering remoto "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="bb47b-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="bb47b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb47b-118">PARAMETERS</span></span>

### <span data-ttu-id="bb47b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb47b-119">-DefaultProfile</span></span>
<span data-ttu-id="bb47b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb47b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bb47b-121">-Force</span></span>
<span data-ttu-id="bb47b-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="bb47b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb47b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb47b-123">-InputObject</span></span>
<span data-ttu-id="bb47b-124">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bb47b-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bb47b-125">-Name</span></span>
<span data-ttu-id="bb47b-126">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="bb47b-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-127">-Principale</span><span class="sxs-lookup"><span data-stu-id="bb47b-127">-Primary</span></span>
<span data-ttu-id="bb47b-128">Rigenerare la chiave primaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="bb47b-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb47b-129">-ResourceGroupName</span></span>
<span data-ttu-id="bb47b-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb47b-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb47b-131">-ResourceId</span></span>
<span data-ttu-id="bb47b-132">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="bb47b-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="bb47b-133">-Secondary</span></span>
<span data-ttu-id="bb47b-134">Rigenerare la chiave primaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="bb47b-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb47b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb47b-135">-Confirm</span></span>
<span data-ttu-id="bb47b-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb47b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb47b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb47b-137">-WhatIf</span></span>
<span data-ttu-id="bb47b-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb47b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb47b-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb47b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb47b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb47b-140">CommonParameters</span></span>
<span data-ttu-id="bb47b-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb47b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bb47b-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb47b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb47b-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb47b-143">INPUTS</span></span>

### <span data-ttu-id="bb47b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bb47b-144">System.String</span></span>

### <span data-ttu-id="bb47b-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="bb47b-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="bb47b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb47b-146">OUTPUTS</span></span>

### <span data-ttu-id="bb47b-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bb47b-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="bb47b-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb47b-148">NOTES</span></span>

## <span data-ttu-id="bb47b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb47b-149">RELATED LINKS</span></span>
