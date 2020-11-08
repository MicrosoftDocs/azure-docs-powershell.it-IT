---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033393"
---
# <span data-ttu-id="07063-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="07063-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="07063-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07063-102">SYNOPSIS</span></span>
<span data-ttu-id="07063-103">Eliminare l'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="07063-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="07063-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07063-104">SYNTAX</span></span>

### <span data-ttu-id="07063-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07063-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07063-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07063-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07063-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="07063-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07063-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07063-108">DESCRIPTION</span></span>
<span data-ttu-id="07063-109">Eliminare l'account di rendering remoto specificato da un determinato gruppo di abbonamenti e risorse.</span><span class="sxs-lookup"><span data-stu-id="07063-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="07063-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07063-110">EXAMPLES</span></span>

### <span data-ttu-id="07063-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07063-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="07063-112">Eliminare l'account di rendering remoto "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="07063-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="07063-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07063-113">PARAMETERS</span></span>

### <span data-ttu-id="07063-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07063-114">-Confirm</span></span>
<span data-ttu-id="07063-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07063-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07063-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07063-116">-DefaultProfile</span></span>
<span data-ttu-id="07063-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07063-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07063-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07063-118">-InputObject</span></span>
<span data-ttu-id="07063-119">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="07063-119">The custom domain object.</span></span>

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

### <span data-ttu-id="07063-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="07063-120">-Name</span></span>
<span data-ttu-id="07063-121">Nome account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="07063-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="07063-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07063-122">-PassThru</span></span>
<span data-ttu-id="07063-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="07063-123">Return object if specified.</span></span>

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

### <span data-ttu-id="07063-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07063-124">-ResourceGroupName</span></span>
<span data-ttu-id="07063-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07063-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="07063-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07063-126">-ResourceId</span></span>
<span data-ttu-id="07063-127">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="07063-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="07063-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07063-128">-WhatIf</span></span>
<span data-ttu-id="07063-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07063-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07063-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07063-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07063-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07063-131">CommonParameters</span></span>
<span data-ttu-id="07063-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07063-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="07063-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07063-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07063-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07063-134">INPUTS</span></span>

### <span data-ttu-id="07063-135">System. String</span><span class="sxs-lookup"><span data-stu-id="07063-135">System.String</span></span>

### <span data-ttu-id="07063-136">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="07063-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="07063-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="07063-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="07063-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07063-138">OUTPUTS</span></span>

### <span data-ttu-id="07063-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07063-139">System.Boolean</span></span>

## <span data-ttu-id="07063-140">Note</span><span class="sxs-lookup"><span data-stu-id="07063-140">NOTES</span></span>

## <span data-ttu-id="07063-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07063-141">RELATED LINKS</span></span>
