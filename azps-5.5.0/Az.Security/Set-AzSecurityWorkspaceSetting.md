---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: a02d2685987844db5f88fafaf12d0c9aed4a3234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201790"
---
# <span data-ttu-id="ec9ae-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="ec9ae-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="ec9ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9ae-103">Aggiorna le impostazioni dell'area di lavoro per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="ec9ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec9ae-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec9ae-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9ae-106">Aggiorna le impostazioni dell'area di lavoro per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="ec9ae-107">L'area di lavoro configurata contenerà i dati di sicurezza raccolti dall'agente di Analisi log di Azure installati nelle macchine virtuali all'interno della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="ec9ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec9ae-108">EXAMPLES</span></span>

### <span data-ttu-id="ec9ae-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec9ae-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="ec9ae-110">Imposta l'area di lavoro "securityuserws" in modo da contenere tutti i dati di sicurezza raccolti dall'agente di Analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="ec9ae-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-111">PARAMETERS</span></span>

### <span data-ttu-id="ec9ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9ae-112">-DefaultProfile</span></span>
<span data-ttu-id="ec9ae-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec9ae-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ec9ae-114">-Name</span></span>
<span data-ttu-id="ec9ae-115">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-115">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="ec9ae-116">-Scope</span></span>
<span data-ttu-id="ec9ae-117">Ambito.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-117">Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ec9ae-118">-WorkspaceId</span></span>
<span data-ttu-id="ec9ae-119">ID area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-119">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec9ae-120">-Confirm</span></span>
<span data-ttu-id="ec9ae-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec9ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec9ae-122">-WhatIf</span></span>
<span data-ttu-id="ec9ae-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec9ae-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec9ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9ae-125">CommonParameters</span></span>
<span data-ttu-id="ec9ae-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9ae-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9ae-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec9ae-128">INPUTS</span></span>

### <span data-ttu-id="ec9ae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ec9ae-129">System.String</span></span>

## <span data-ttu-id="ec9ae-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec9ae-130">OUTPUTS</span></span>

### <span data-ttu-id="ec9ae-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="ec9ae-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="ec9ae-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec9ae-132">NOTES</span></span>

## <span data-ttu-id="ec9ae-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec9ae-133">RELATED LINKS</span></span>
