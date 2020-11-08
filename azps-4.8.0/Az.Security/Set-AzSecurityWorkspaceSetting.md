---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 23d35a0bce62aa2a3a5c922ea0e25e35cb619b09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188833"
---
# <span data-ttu-id="97fcb-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="97fcb-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="97fcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="97fcb-103">Aggiorna le impostazioni dell'area di lavoro per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97fcb-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="97fcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97fcb-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97fcb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="97fcb-106">Aggiorna le impostazioni dell'area di lavoro per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97fcb-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="97fcb-107">L'area di lavoro configurata conterrà i dati di sicurezza raccolti dall'agente di analisi del log di Azure che è installato in VM all'interno di questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97fcb-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="97fcb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97fcb-108">EXAMPLES</span></span>

### <span data-ttu-id="97fcb-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97fcb-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="97fcb-110">Imposta l'area di lavoro "area di lavoro" per contenere tutti i dati di sicurezza raccolti dall'agente di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="97fcb-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="97fcb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97fcb-111">PARAMETERS</span></span>

### <span data-ttu-id="97fcb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fcb-112">-DefaultProfile</span></span>
<span data-ttu-id="97fcb-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97fcb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97fcb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="97fcb-114">-Name</span></span>
<span data-ttu-id="97fcb-115">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="97fcb-115">Resource name.</span></span>

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

### <span data-ttu-id="97fcb-116">-Ambito</span><span class="sxs-lookup"><span data-stu-id="97fcb-116">-Scope</span></span>
<span data-ttu-id="97fcb-117">Ambito.</span><span class="sxs-lookup"><span data-stu-id="97fcb-117">Scope.</span></span>

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

### <span data-ttu-id="97fcb-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="97fcb-118">-WorkspaceId</span></span>
<span data-ttu-id="97fcb-119">ID area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="97fcb-119">Workspace ID.</span></span>

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

### <span data-ttu-id="97fcb-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97fcb-120">-Confirm</span></span>
<span data-ttu-id="97fcb-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97fcb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97fcb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97fcb-122">-WhatIf</span></span>
<span data-ttu-id="97fcb-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97fcb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97fcb-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97fcb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97fcb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fcb-125">CommonParameters</span></span>
<span data-ttu-id="97fcb-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97fcb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fcb-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97fcb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fcb-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97fcb-128">INPUTS</span></span>

### <span data-ttu-id="97fcb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="97fcb-129">System.String</span></span>

## <span data-ttu-id="97fcb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97fcb-130">OUTPUTS</span></span>

### <span data-ttu-id="97fcb-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="97fcb-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="97fcb-132">Note</span><span class="sxs-lookup"><span data-stu-id="97fcb-132">NOTES</span></span>

## <span data-ttu-id="97fcb-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97fcb-133">RELATED LINKS</span></span>
