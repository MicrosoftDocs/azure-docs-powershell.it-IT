---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475584"
---
# <span data-ttu-id="1dce3-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="1dce3-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="1dce3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dce3-102">SYNOPSIS</span></span>
<span data-ttu-id="1dce3-103">Chiave di rigenerazione dell'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="1dce3-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="1dce3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dce3-104">SYNTAX</span></span>

### <span data-ttu-id="1dce3-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dce3-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dce3-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dce3-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dce3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dce3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dce3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dce3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dce3-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dce3-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dce3-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dce3-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dce3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dce3-111">DESCRIPTION</span></span>
<span data-ttu-id="1dce3-112">Rigenera una chiave primaria o una chiave secondaria di un account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="1dce3-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="1dce3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dce3-113">EXAMPLES</span></span>

### <span data-ttu-id="1dce3-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dce3-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="1dce3-115">Rigenera chiave secondaria di un account di rendering remoto "esempio" nel gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="1dce3-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="1dce3-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1dce3-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="1dce3-117">Rigenerazione della chiave secondaria dell'account di rendering remoto "esempio" dal gruppo di risorse e dell'abbonamento corrente "RG1" con piping.</span><span class="sxs-lookup"><span data-stu-id="1dce3-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="1dce3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dce3-118">PARAMETERS</span></span>

### <span data-ttu-id="1dce3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dce3-119">-DefaultProfile</span></span>
<span data-ttu-id="1dce3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dce3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dce3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1dce3-121">-Force</span></span>
<span data-ttu-id="1dce3-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1dce3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dce3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dce3-123">-InputObject</span></span>
<span data-ttu-id="1dce3-124">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1dce3-124">The custom domain object.</span></span>

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

### <span data-ttu-id="1dce3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dce3-125">-Name</span></span>
<span data-ttu-id="1dce3-126">Nome account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="1dce3-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="1dce3-127">-Primaria</span><span class="sxs-lookup"><span data-stu-id="1dce3-127">-Primary</span></span>
<span data-ttu-id="1dce3-128">Rigenera la chiave primaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="1dce3-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="1dce3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dce3-129">-ResourceGroupName</span></span>
<span data-ttu-id="1dce3-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dce3-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="1dce3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dce3-131">-ResourceId</span></span>
<span data-ttu-id="1dce3-132">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="1dce3-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="1dce3-133">-Secondario</span><span class="sxs-lookup"><span data-stu-id="1dce3-133">-Secondary</span></span>
<span data-ttu-id="1dce3-134">Rigenera la chiave primaria dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="1dce3-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="1dce3-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dce3-135">-Confirm</span></span>
<span data-ttu-id="1dce3-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dce3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dce3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dce3-137">-WhatIf</span></span>
<span data-ttu-id="1dce3-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dce3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dce3-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dce3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dce3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dce3-140">CommonParameters</span></span>
<span data-ttu-id="1dce3-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dce3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1dce3-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dce3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dce3-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dce3-143">INPUTS</span></span>

### <span data-ttu-id="1dce3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1dce3-144">System.String</span></span>

### <span data-ttu-id="1dce3-145">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="1dce3-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="1dce3-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dce3-146">OUTPUTS</span></span>

### <span data-ttu-id="1dce3-147">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1dce3-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="1dce3-148">Note</span><span class="sxs-lookup"><span data-stu-id="1dce3-148">NOTES</span></span>

## <span data-ttu-id="1dce3-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dce3-149">RELATED LINKS</span></span>
