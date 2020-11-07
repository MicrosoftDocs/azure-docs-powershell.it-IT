---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: c52a6f7ee513f67d838de5a8c049227c5fc4ad64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677193"
---
# <span data-ttu-id="5fb23-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5fb23-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5fb23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fb23-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb23-103">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5fb23-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="5fb23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fb23-104">SYNTAX</span></span>

### <span data-ttu-id="5fb23-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fb23-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb23-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb23-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb23-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5fb23-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb23-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fb23-108">DESCRIPTION</span></span>
<span data-ttu-id="5fb23-109">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5fb23-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="5fb23-110">Questa azione consentirà agli agenti di sicurezza appena installati di segnalare l'area di lavoro predefinita di questo susbscription.</span><span class="sxs-lookup"><span data-stu-id="5fb23-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="5fb23-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fb23-111">EXAMPLES</span></span>

### <span data-ttu-id="5fb23-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5fb23-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="5fb23-113">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5fb23-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="5fb23-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fb23-114">PARAMETERS</span></span>

### <span data-ttu-id="5fb23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb23-115">-DefaultProfile</span></span>
<span data-ttu-id="5fb23-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb23-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fb23-117">-InputObject</span></span>
<span data-ttu-id="5fb23-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="5fb23-118">Input Object.</span></span>

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

### <span data-ttu-id="5fb23-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fb23-119">-Name</span></span>
<span data-ttu-id="5fb23-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="5fb23-120">Resource name.</span></span>

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

### <span data-ttu-id="5fb23-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fb23-121">-PassThru</span></span>
<span data-ttu-id="5fb23-122">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="5fb23-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5fb23-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb23-123">-ResourceId</span></span>
<span data-ttu-id="5fb23-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5fb23-124">Resource ID.</span></span>

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

### <span data-ttu-id="5fb23-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5fb23-125">-Confirm</span></span>
<span data-ttu-id="5fb23-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fb23-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb23-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb23-127">-WhatIf</span></span>
<span data-ttu-id="5fb23-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fb23-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fb23-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fb23-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb23-130">CommonParameters</span></span>
<span data-ttu-id="5fb23-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb23-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb23-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb23-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fb23-133">INPUTS</span></span>

### <span data-ttu-id="5fb23-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb23-134">System.String</span></span>

### <span data-ttu-id="5fb23-135">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5fb23-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5fb23-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fb23-136">OUTPUTS</span></span>

### <span data-ttu-id="5fb23-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fb23-137">System.Boolean</span></span>

## <span data-ttu-id="5fb23-138">Note</span><span class="sxs-lookup"><span data-stu-id="5fb23-138">NOTES</span></span>

## <span data-ttu-id="5fb23-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fb23-139">RELATED LINKS</span></span>
