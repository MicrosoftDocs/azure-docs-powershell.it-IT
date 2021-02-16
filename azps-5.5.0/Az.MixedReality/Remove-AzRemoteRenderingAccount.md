---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185007"
---
# <span data-ttu-id="c6fe7-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="c6fe7-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="c6fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fe7-103">Elimina account rendering remoto</span><span class="sxs-lookup"><span data-stu-id="c6fe7-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="c6fe7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6fe7-104">SYNTAX</span></span>

### <span data-ttu-id="c6fe7-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c6fe7-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6fe7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6fe7-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6fe7-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6fe7-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6fe7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6fe7-108">DESCRIPTION</span></span>
<span data-ttu-id="c6fe7-109">Eliminare l'account di rendering remoto specificato da determinati gruppi di risorse e sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="c6fe7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6fe7-110">EXAMPLES</span></span>

### <span data-ttu-id="c6fe7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6fe7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="c6fe7-112">Eliminare l'account di rendering remoto "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="c6fe7-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="c6fe7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6fe7-113">PARAMETERS</span></span>

### <span data-ttu-id="c6fe7-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6fe7-114">-Confirm</span></span>
<span data-ttu-id="c6fe7-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6fe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fe7-116">-DefaultProfile</span></span>
<span data-ttu-id="c6fe7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6fe7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6fe7-118">-InputObject</span></span>
<span data-ttu-id="c6fe7-119">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-119">The custom domain object.</span></span>

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

### <span data-ttu-id="c6fe7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c6fe7-120">-Name</span></span>
<span data-ttu-id="c6fe7-121">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="c6fe7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6fe7-122">-PassThru</span></span>
<span data-ttu-id="c6fe7-123">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-123">Return object if specified.</span></span>

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

### <span data-ttu-id="c6fe7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6fe7-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6fe7-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6fe7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6fe7-126">-ResourceId</span></span>
<span data-ttu-id="c6fe7-127">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="c6fe7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6fe7-128">-WhatIf</span></span>
<span data-ttu-id="c6fe7-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6fe7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6fe7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fe7-131">CommonParameters</span></span>
<span data-ttu-id="c6fe7-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6fe7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c6fe7-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6fe7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fe7-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6fe7-134">INPUTS</span></span>

### <span data-ttu-id="c6fe7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c6fe7-135">System.String</span></span>

### <span data-ttu-id="c6fe7-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="c6fe7-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="c6fe7-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c6fe7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c6fe7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6fe7-138">OUTPUTS</span></span>

### <span data-ttu-id="c6fe7-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6fe7-139">System.Boolean</span></span>

## <span data-ttu-id="c6fe7-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6fe7-140">NOTES</span></span>

## <span data-ttu-id="c6fe7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6fe7-141">RELATED LINKS</span></span>
