---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: ef14039cc1f46c3a891090475814d6e9553da431
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006541"
---
# <span data-ttu-id="7cdbc-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7cdbc-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="7cdbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cdbc-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdbc-103">Elimina account per rendering remoto</span><span class="sxs-lookup"><span data-stu-id="7cdbc-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="7cdbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cdbc-104">SYNTAX</span></span>

### <span data-ttu-id="7cdbc-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7cdbc-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cdbc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cdbc-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cdbc-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cdbc-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cdbc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7cdbc-108">DESCRIPTION</span></span>
<span data-ttu-id="7cdbc-109">Eliminare l'account di rendering remoto specificato da determinati gruppi di risorse e sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="7cdbc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cdbc-110">EXAMPLES</span></span>

### <span data-ttu-id="7cdbc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7cdbc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="7cdbc-112">Eliminare l'account di rendering remoto "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="7cdbc-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="7cdbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cdbc-113">PARAMETERS</span></span>

### <span data-ttu-id="7cdbc-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cdbc-114">-Confirm</span></span>
<span data-ttu-id="7cdbc-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdbc-116">-DefaultProfile</span></span>
<span data-ttu-id="7cdbc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cdbc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cdbc-118">-InputObject</span></span>
<span data-ttu-id="7cdbc-119">Oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7cdbc-120">-Name</span></span>
<span data-ttu-id="7cdbc-121">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cdbc-122">-PassThru</span></span>
<span data-ttu-id="7cdbc-123">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cdbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="7cdbc-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cdbc-126">-ResourceId</span></span>
<span data-ttu-id="7cdbc-127">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cdbc-128">-WhatIf</span></span>
<span data-ttu-id="7cdbc-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cdbc-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdbc-131">CommonParameters</span></span>
<span data-ttu-id="7cdbc-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cdbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7cdbc-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cdbc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdbc-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="7cdbc-134">INPUTS</span></span>

### <span data-ttu-id="7cdbc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7cdbc-135">System.String</span></span>

### <span data-ttu-id="7cdbc-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7cdbc-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="7cdbc-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cdbc-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7cdbc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cdbc-138">OUTPUTS</span></span>

### <span data-ttu-id="7cdbc-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7cdbc-139">System.Boolean</span></span>

## <span data-ttu-id="7cdbc-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="7cdbc-140">NOTES</span></span>

## <span data-ttu-id="7cdbc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cdbc-141">RELATED LINKS</span></span>
