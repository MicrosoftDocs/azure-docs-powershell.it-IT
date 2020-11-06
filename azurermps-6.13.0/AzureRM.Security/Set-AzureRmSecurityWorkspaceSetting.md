---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518568"
---
# <span data-ttu-id="7b784-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="7b784-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="7b784-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b784-102">SYNOPSIS</span></span>
<span data-ttu-id="7b784-103">Aggiorna le impostazioni dell'area di lavoro per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b784-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b784-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b784-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b784-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b784-105">DESCRIPTION</span></span>
<span data-ttu-id="7b784-106">Aggiorna le impostazioni dell'area di lavoro per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b784-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="7b784-107">L'area di lavoro configurata conterrà i dati di sicurezza raccolti dall'agente di sicurezza installato in VM all'interno di questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b784-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="7b784-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b784-108">EXAMPLES</span></span>

### <span data-ttu-id="7b784-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b784-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="7b784-110">Imposta l'area di lavoro "area di lavoro" per contenere tutti i dati di sicurezza raccolti dagli agenti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7b784-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="7b784-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b784-111">PARAMETERS</span></span>

### <span data-ttu-id="7b784-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b784-112">-DefaultProfile</span></span>
<span data-ttu-id="7b784-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b784-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b784-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b784-114">-Name</span></span>
<span data-ttu-id="7b784-115">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b784-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b784-116">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7b784-116">-Scope</span></span>
<span data-ttu-id="7b784-117">Ambito.</span><span class="sxs-lookup"><span data-stu-id="7b784-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b784-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7b784-118">-WorkspaceId</span></span>
<span data-ttu-id="7b784-119">ID area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7b784-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b784-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b784-120">-Confirm</span></span>
<span data-ttu-id="7b784-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b784-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b784-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b784-122">-WhatIf</span></span>
<span data-ttu-id="7b784-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b784-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b784-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b784-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b784-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b784-125">CommonParameters</span></span>
<span data-ttu-id="7b784-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b784-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b784-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b784-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b784-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b784-128">INPUTS</span></span>

### <span data-ttu-id="7b784-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b784-129">System.String</span></span>

## <span data-ttu-id="7b784-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b784-130">OUTPUTS</span></span>

### <span data-ttu-id="7b784-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="7b784-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="7b784-132">Note</span><span class="sxs-lookup"><span data-stu-id="7b784-132">NOTES</span></span>

## <span data-ttu-id="7b784-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b784-133">RELATED LINKS</span></span>
