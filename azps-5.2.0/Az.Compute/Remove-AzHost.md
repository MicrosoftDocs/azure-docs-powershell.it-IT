---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365172"
---
# <span data-ttu-id="ca00d-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ca00d-101">Remove-AzHost</span></span>

## <span data-ttu-id="ca00d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca00d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca00d-103">Rimuove un host.</span><span class="sxs-lookup"><span data-stu-id="ca00d-103">Removes a host.</span></span>

## <span data-ttu-id="ca00d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca00d-104">SYNTAX</span></span>

### <span data-ttu-id="ca00d-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca00d-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca00d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ca00d-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca00d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ca00d-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca00d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca00d-108">DESCRIPTION</span></span>
<span data-ttu-id="ca00d-109">Questo cmdlet eliminerà un host</span><span class="sxs-lookup"><span data-stu-id="ca00d-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="ca00d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca00d-110">EXAMPLES</span></span>

### <span data-ttu-id="ca00d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca00d-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="ca00d-112">Questo comando consente di ottenere e rimuovere l'host indicato.</span><span class="sxs-lookup"><span data-stu-id="ca00d-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="ca00d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ca00d-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="ca00d-114">Questo comando rimuove l'host indicato.</span><span class="sxs-lookup"><span data-stu-id="ca00d-114">This command removes the given host.</span></span>

## <span data-ttu-id="ca00d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca00d-115">PARAMETERS</span></span>

### <span data-ttu-id="ca00d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca00d-116">-AsJob</span></span>
<span data-ttu-id="ca00d-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca00d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca00d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca00d-118">-DefaultProfile</span></span>
<span data-ttu-id="ca00d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca00d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca00d-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="ca00d-120">-HostGroupName</span></span>
<span data-ttu-id="ca00d-121">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="ca00d-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca00d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca00d-122">-InputObject</span></span>
<span data-ttu-id="ca00d-123">Oggetto local dell'host.</span><span class="sxs-lookup"><span data-stu-id="ca00d-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca00d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca00d-124">-Name</span></span>
<span data-ttu-id="ca00d-125">Nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="ca00d-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca00d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca00d-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca00d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca00d-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca00d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca00d-128">-ResourceId</span></span>
<span data-ttu-id="ca00d-129">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca00d-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca00d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca00d-130">-Confirm</span></span>
<span data-ttu-id="ca00d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca00d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca00d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca00d-132">-WhatIf</span></span>
<span data-ttu-id="ca00d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca00d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca00d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca00d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca00d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca00d-135">CommonParameters</span></span>
<span data-ttu-id="ca00d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca00d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca00d-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca00d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca00d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca00d-138">INPUTS</span></span>

### <span data-ttu-id="ca00d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ca00d-139">System.String</span></span>

### <span data-ttu-id="ca00d-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="ca00d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="ca00d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca00d-141">OUTPUTS</span></span>

### <span data-ttu-id="ca00d-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ca00d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ca00d-143">Note</span><span class="sxs-lookup"><span data-stu-id="ca00d-143">NOTES</span></span>

## <span data-ttu-id="ca00d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca00d-144">RELATED LINKS</span></span>
