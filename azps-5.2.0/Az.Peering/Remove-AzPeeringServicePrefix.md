---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338047"
---
# <span data-ttu-id="750fc-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="750fc-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="750fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="750fc-102">SYNOPSIS</span></span>
<span data-ttu-id="750fc-103">Rimuove un nuovo prefisso del servizio peering</span><span class="sxs-lookup"><span data-stu-id="750fc-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="750fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="750fc-104">SYNTAX</span></span>

### <span data-ttu-id="750fc-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="750fc-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750fc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="750fc-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750fc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="750fc-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="750fc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="750fc-108">DESCRIPTION</span></span>
<span data-ttu-id="750fc-109">Rimuove un prefisso del servizio peer da un servizio peering.</span><span class="sxs-lookup"><span data-stu-id="750fc-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="750fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="750fc-110">EXAMPLES</span></span>

### <span data-ttu-id="750fc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="750fc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="750fc-112">Rimuovere un prefisso da un oggetto servizio peering</span><span class="sxs-lookup"><span data-stu-id="750fc-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="750fc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="750fc-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="750fc-114">Rimuovere un prefisso da un ID di risorsa del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="750fc-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="750fc-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="750fc-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="750fc-116">Rimuovere un prefisso da un nome e un nome del gruppo di risorse del servizio peer</span><span class="sxs-lookup"><span data-stu-id="750fc-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="750fc-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="750fc-117">PARAMETERS</span></span>

### <span data-ttu-id="750fc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="750fc-118">-AsJob</span></span>
<span data-ttu-id="750fc-119">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="750fc-119">Run in the background.</span></span>

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

### <span data-ttu-id="750fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750fc-120">-DefaultProfile</span></span>
<span data-ttu-id="750fc-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="750fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="750fc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="750fc-122">-Force</span></span>
<span data-ttu-id="750fc-123">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="750fc-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="750fc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="750fc-124">-InputObject</span></span>
<span data-ttu-id="750fc-125">Usare un Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="750fc-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="750fc-126">-Name</span></span>
<span data-ttu-id="750fc-127">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="750fc-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="750fc-128">-PassThru</span></span>
<span data-ttu-id="750fc-129">Restituisce vero per Success o false per failed.</span><span class="sxs-lookup"><span data-stu-id="750fc-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="750fc-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="750fc-130">-PrefixName</span></span>
<span data-ttu-id="750fc-131">Il nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="750fc-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="750fc-132">-ResourceGroupName</span></span>
<span data-ttu-id="750fc-133">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="750fc-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="750fc-134">-ResourceId</span></span>
<span data-ttu-id="750fc-135">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="750fc-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750fc-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="750fc-136">-Confirm</span></span>
<span data-ttu-id="750fc-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="750fc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="750fc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="750fc-138">-WhatIf</span></span>
<span data-ttu-id="750fc-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="750fc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="750fc-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="750fc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="750fc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750fc-141">CommonParameters</span></span>
<span data-ttu-id="750fc-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="750fc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750fc-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="750fc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750fc-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="750fc-144">INPUTS</span></span>

### <span data-ttu-id="750fc-145">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="750fc-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="750fc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="750fc-146">System.String</span></span>

## <span data-ttu-id="750fc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="750fc-147">OUTPUTS</span></span>

### <span data-ttu-id="750fc-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="750fc-148">System.Boolean</span></span>

## <span data-ttu-id="750fc-149">Note</span><span class="sxs-lookup"><span data-stu-id="750fc-149">NOTES</span></span>

## <span data-ttu-id="750fc-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="750fc-150">RELATED LINKS</span></span>
