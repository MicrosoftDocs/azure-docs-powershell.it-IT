---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201472"
---
# <span data-ttu-id="4f74b-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4f74b-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4f74b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f74b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f74b-103">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f74b-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="4f74b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f74b-104">SYNTAX</span></span>

### <span data-ttu-id="4f74b-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f74b-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f74b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f74b-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f74b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4f74b-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f74b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f74b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f74b-109">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f74b-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="4f74b-110">Questa azione consentirà agli agenti di sicurezza appena installati di segnalare l'area di lavoro predefinita di questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f74b-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="4f74b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f74b-111">EXAMPLES</span></span>

### <span data-ttu-id="4f74b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f74b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="4f74b-113">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f74b-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="4f74b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f74b-114">PARAMETERS</span></span>

### <span data-ttu-id="4f74b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f74b-115">-DefaultProfile</span></span>
<span data-ttu-id="4f74b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f74b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f74b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f74b-117">-InputObject</span></span>
<span data-ttu-id="4f74b-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="4f74b-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f74b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f74b-119">-Name</span></span>
<span data-ttu-id="4f74b-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f74b-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f74b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f74b-121">-PassThru</span></span>
<span data-ttu-id="4f74b-122">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="4f74b-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="4f74b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f74b-123">-ResourceId</span></span>
<span data-ttu-id="4f74b-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f74b-124">Resource ID.</span></span>

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

### <span data-ttu-id="4f74b-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f74b-125">-Confirm</span></span>
<span data-ttu-id="4f74b-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f74b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f74b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f74b-127">-WhatIf</span></span>
<span data-ttu-id="4f74b-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f74b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f74b-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f74b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f74b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f74b-130">CommonParameters</span></span>
<span data-ttu-id="4f74b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f74b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f74b-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f74b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f74b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f74b-133">INPUTS</span></span>

### <span data-ttu-id="4f74b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4f74b-134">System.String</span></span>

### <span data-ttu-id="4f74b-135">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4f74b-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4f74b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f74b-136">OUTPUTS</span></span>

### <span data-ttu-id="4f74b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f74b-137">System.Boolean</span></span>

## <span data-ttu-id="4f74b-138">Note</span><span class="sxs-lookup"><span data-stu-id="4f74b-138">NOTES</span></span>

## <span data-ttu-id="4f74b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f74b-139">RELATED LINKS</span></span>
