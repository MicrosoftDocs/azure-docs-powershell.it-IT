---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191933"
---
# <span data-ttu-id="e9d84-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e9d84-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="e9d84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9d84-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d84-103">Eliminare la soluzione di sicurezza degli Stati</span><span class="sxs-lookup"><span data-stu-id="e9d84-103">Delete IoT security solution</span></span>

## <span data-ttu-id="e9d84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9d84-104">SYNTAX</span></span>

### <span data-ttu-id="e9d84-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9d84-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d84-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9d84-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9d84-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e9d84-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9d84-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9d84-108">DESCRIPTION</span></span>
<span data-ttu-id="e9d84-109">Il cmdlet Remove-AzIotSecuritySolution Elimina una specifica soluzione di sicurezza per gli altri.</span><span class="sxs-lookup"><span data-stu-id="e9d84-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="e9d84-110">La soluzione per la sicurezza degli argomenti raccoglie i dati di sicurezza e gli eventi provenienti da dispositivi molto e hub per evitare e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="e9d84-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="e9d84-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9d84-111">EXAMPLES</span></span>

### <span data-ttu-id="e9d84-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9d84-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e9d84-113">Eliminare la soluzione di sicurezza degli altri "esempio" con il gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e9d84-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e9d84-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9d84-114">PARAMETERS</span></span>

### <span data-ttu-id="e9d84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d84-115">-DefaultProfile</span></span>
<span data-ttu-id="e9d84-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9d84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d84-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9d84-117">-InputObject</span></span>
<span data-ttu-id="e9d84-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="e9d84-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d84-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9d84-119">-Name</span></span>
<span data-ttu-id="e9d84-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="e9d84-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d84-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9d84-121">-PassThru</span></span>
<span data-ttu-id="e9d84-122">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="e9d84-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e9d84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d84-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9d84-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9d84-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9d84-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9d84-125">-ResourceId</span></span>
<span data-ttu-id="e9d84-126">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="e9d84-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9d84-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9d84-127">-Confirm</span></span>
<span data-ttu-id="e9d84-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9d84-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9d84-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9d84-129">-WhatIf</span></span>
<span data-ttu-id="e9d84-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9d84-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9d84-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9d84-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9d84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d84-132">CommonParameters</span></span>
<span data-ttu-id="e9d84-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d84-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9d84-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d84-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9d84-135">INPUTS</span></span>

### <span data-ttu-id="e9d84-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e9d84-136">System.String</span></span>

### <span data-ttu-id="e9d84-137">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e9d84-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="e9d84-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9d84-138">OUTPUTS</span></span>

### <span data-ttu-id="e9d84-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9d84-139">System.Boolean</span></span>

## <span data-ttu-id="e9d84-140">Note</span><span class="sxs-lookup"><span data-stu-id="e9d84-140">NOTES</span></span>

## <span data-ttu-id="e9d84-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9d84-141">RELATED LINKS</span></span>