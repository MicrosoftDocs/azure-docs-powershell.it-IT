---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686043"
---
# <span data-ttu-id="8b8a9-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="8b8a9-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="8b8a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8a9-103">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b8a9-104">SYNTAX</span></span>

### <span data-ttu-id="8b8a9-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b8a9-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8a9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b8a9-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8a9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8b8a9-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b8a9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b8a9-108">DESCRIPTION</span></span>
<span data-ttu-id="8b8a9-109">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="8b8a9-110">Questa azione consentirà agli agenti di sicurezza appena installati di segnalare l'area di lavoro predefinita di questo susbscription.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="8b8a9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b8a9-111">EXAMPLES</span></span>

### <span data-ttu-id="8b8a9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b8a9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="8b8a9-113">Elimina l'impostazione dell'area di lavoro sicurezza per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="8b8a9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b8a9-114">PARAMETERS</span></span>

### <span data-ttu-id="8b8a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8a9-115">-DefaultProfile</span></span>
<span data-ttu-id="8b8a9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b8a9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b8a9-117">-InputObject</span></span>
<span data-ttu-id="8b8a9-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b8a9-119">-Name</span></span>
<span data-ttu-id="8b8a9-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b8a9-121">-PassThru</span></span>
<span data-ttu-id="8b8a9-122">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b8a9-123">-ResourceId</span></span>
<span data-ttu-id="8b8a9-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-124">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8a9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b8a9-125">-Confirm</span></span>
<span data-ttu-id="8b8a9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b8a9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b8a9-127">-WhatIf</span></span>
<span data-ttu-id="8b8a9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b8a9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b8a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8a9-130">CommonParameters</span></span>
<span data-ttu-id="8b8a9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b8a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8a9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8a9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b8a9-133">INPUTS</span></span>

### <span data-ttu-id="8b8a9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8b8a9-134">System.String</span></span>
<span data-ttu-id="8b8a9-135">Microsoft. Azure. Commands. Security. Cmdlets. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="8b8a9-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="8b8a9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b8a9-136">OUTPUTS</span></span>

### <span data-ttu-id="8b8a9-137">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="8b8a9-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="8b8a9-138">Note</span><span class="sxs-lookup"><span data-stu-id="8b8a9-138">NOTES</span></span>

## <span data-ttu-id="8b8a9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b8a9-139">RELATED LINKS</span></span>
