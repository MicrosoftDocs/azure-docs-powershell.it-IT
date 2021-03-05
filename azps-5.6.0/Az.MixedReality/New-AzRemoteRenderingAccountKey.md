---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 8bfc07b5502c2dd648beea827af9587c9e6d9447
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970526"
---
# <span data-ttu-id="98311-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="98311-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="98311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98311-102">SYNOPSIS</span></span>
<span data-ttu-id="98311-103">Rigenerare la chiave dell'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="98311-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="98311-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98311-104">SYNTAX</span></span>

### <span data-ttu-id="98311-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="98311-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98311-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="98311-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98311-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="98311-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98311-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="98311-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98311-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="98311-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98311-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="98311-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98311-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98311-111">DESCRIPTION</span></span>
<span data-ttu-id="98311-112">Rigenerare la chiave primaria o la chiave secondaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="98311-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="98311-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98311-113">EXAMPLES</span></span>

### <span data-ttu-id="98311-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98311-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="98311-115">Rigenerare la chiave secondaria dell'account di rendering remoto "example" nel gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="98311-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="98311-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="98311-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="98311-117">Rigenerare la chiave secondaria dell'account di rendering remoto "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="98311-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="98311-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98311-118">PARAMETERS</span></span>

### <span data-ttu-id="98311-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98311-119">-DefaultProfile</span></span>
<span data-ttu-id="98311-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98311-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98311-121">-Force</span><span class="sxs-lookup"><span data-stu-id="98311-121">-Force</span></span>
<span data-ttu-id="98311-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="98311-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98311-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98311-123">-InputObject</span></span>
<span data-ttu-id="98311-124">Oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="98311-124">The custom domain object.</span></span>

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

### <span data-ttu-id="98311-125">-Name</span><span class="sxs-lookup"><span data-stu-id="98311-125">-Name</span></span>
<span data-ttu-id="98311-126">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="98311-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="98311-127">-Principale</span><span class="sxs-lookup"><span data-stu-id="98311-127">-Primary</span></span>
<span data-ttu-id="98311-128">Rigenerare la chiave primaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="98311-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="98311-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98311-129">-ResourceGroupName</span></span>
<span data-ttu-id="98311-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="98311-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="98311-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98311-131">-ResourceId</span></span>
<span data-ttu-id="98311-132">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="98311-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="98311-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="98311-133">-Secondary</span></span>
<span data-ttu-id="98311-134">Rigenerare la chiave primaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="98311-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="98311-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98311-135">-Confirm</span></span>
<span data-ttu-id="98311-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98311-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98311-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98311-137">-WhatIf</span></span>
<span data-ttu-id="98311-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98311-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98311-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98311-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98311-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98311-140">CommonParameters</span></span>
<span data-ttu-id="98311-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98311-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98311-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98311-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98311-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="98311-143">INPUTS</span></span>

### <span data-ttu-id="98311-144">System.String</span><span class="sxs-lookup"><span data-stu-id="98311-144">System.String</span></span>

### <span data-ttu-id="98311-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="98311-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="98311-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98311-146">OUTPUTS</span></span>

### <span data-ttu-id="98311-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98311-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="98311-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="98311-148">NOTES</span></span>

## <span data-ttu-id="98311-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98311-149">RELATED LINKS</span></span>
