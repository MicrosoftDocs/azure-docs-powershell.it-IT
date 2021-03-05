---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: b351cfaa5d94c7104972158dc9dee6363a7d466b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984078"
---
# <span data-ttu-id="c24fd-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c24fd-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c24fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c24fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c24fd-103">Elimina l'impostazione dell'area di lavoro di sicurezza per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24fd-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="c24fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c24fd-104">SYNTAX</span></span>

### <span data-ttu-id="c24fd-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="c24fd-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24fd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c24fd-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24fd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c24fd-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c24fd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c24fd-108">DESCRIPTION</span></span>
<span data-ttu-id="c24fd-109">Elimina l'impostazione dell'area di lavoro di sicurezza per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24fd-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="c24fd-110">Questa azione consente agli agenti di sicurezza appena installati di segnalare l'area di lavoro predefinita di questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24fd-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="c24fd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c24fd-111">EXAMPLES</span></span>

### <span data-ttu-id="c24fd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c24fd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="c24fd-113">Elimina l'impostazione dell'area di lavoro di sicurezza per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24fd-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="c24fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c24fd-114">PARAMETERS</span></span>

### <span data-ttu-id="c24fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24fd-115">-DefaultProfile</span></span>
<span data-ttu-id="c24fd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c24fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c24fd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c24fd-117">-InputObject</span></span>
<span data-ttu-id="c24fd-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="c24fd-118">Input Object.</span></span>

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

### <span data-ttu-id="c24fd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c24fd-119">-Name</span></span>
<span data-ttu-id="c24fd-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c24fd-120">Resource name.</span></span>

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

### <span data-ttu-id="c24fd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c24fd-121">-PassThru</span></span>
<span data-ttu-id="c24fd-122">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="c24fd-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="c24fd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c24fd-123">-ResourceId</span></span>
<span data-ttu-id="c24fd-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c24fd-124">Resource ID.</span></span>

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

### <span data-ttu-id="c24fd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c24fd-125">-Confirm</span></span>
<span data-ttu-id="c24fd-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c24fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c24fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24fd-127">-WhatIf</span></span>
<span data-ttu-id="c24fd-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c24fd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c24fd-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c24fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c24fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24fd-130">CommonParameters</span></span>
<span data-ttu-id="c24fd-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24fd-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c24fd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24fd-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c24fd-133">INPUTS</span></span>

### <span data-ttu-id="c24fd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c24fd-134">System.String</span></span>

### <span data-ttu-id="c24fd-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c24fd-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c24fd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c24fd-136">OUTPUTS</span></span>

### <span data-ttu-id="c24fd-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c24fd-137">System.Boolean</span></span>

## <span data-ttu-id="c24fd-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c24fd-138">NOTES</span></span>

## <span data-ttu-id="c24fd-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c24fd-139">RELATED LINKS</span></span>
