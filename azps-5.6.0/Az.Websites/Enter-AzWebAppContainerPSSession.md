---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: e889e3f8d3d94993494c10141629eee6dceed01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972382"
---
# <span data-ttu-id="3fb64-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="3fb64-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="3fb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fb64-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb64-103">Apre una sessione di PowerShell remota nel contenitore di windows specificato in un determinato sito o slot e in un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3fb64-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="3fb64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fb64-104">SYNTAX</span></span>

### <span data-ttu-id="3fb64-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fb64-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb64-106">S2</span><span class="sxs-lookup"><span data-stu-id="3fb64-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fb64-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3fb64-107">DESCRIPTION</span></span>
<span data-ttu-id="3fb64-108">apre una sessione di PowerShell remota nel contenitore di windows specificato in un determinato sito o slot e in un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3fb64-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="3fb64-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fb64-109">EXAMPLES</span></span>

### <span data-ttu-id="3fb64-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3fb64-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="3fb64-111">Questo comando apre una sessione di PowerShell remota nell'app contenitore di windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="3fb64-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="3fb64-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fb64-112">PARAMETERS</span></span>

### <span data-ttu-id="3fb64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb64-113">-DefaultProfile</span></span>
<span data-ttu-id="3fb64-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb64-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fb64-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3fb64-115">-Force</span></span>
<span data-ttu-id="3fb64-116">Creare la sessione di PowerShell senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3fb64-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3fb64-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3fb64-117">-Name</span></span>
<span data-ttu-id="3fb64-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="3fb64-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb64-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fb64-119">-PassThru</span></span>
<span data-ttu-id="3fb64-120">Restituisce un valore che indica un'operazione riuscita o non riuscita</span><span class="sxs-lookup"><span data-stu-id="3fb64-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="3fb64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb64-121">-ResourceGroupName</span></span>
<span data-ttu-id="3fb64-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3fb64-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb64-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="3fb64-123">-SlotName</span></span>
<span data-ttu-id="3fb64-124">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="3fb64-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb64-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3fb64-125">-WebApp</span></span>
<span data-ttu-id="3fb64-126">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="3fb64-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb64-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fb64-127">-Confirm</span></span>
<span data-ttu-id="3fb64-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fb64-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb64-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb64-129">-WhatIf</span></span>
<span data-ttu-id="3fb64-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fb64-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fb64-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fb64-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb64-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb64-132">CommonParameters</span></span>
<span data-ttu-id="3fb64-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb64-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb64-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fb64-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb64-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="3fb64-135">INPUTS</span></span>

### <span data-ttu-id="3fb64-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3fb64-136">System.String</span></span>

### <span data-ttu-id="3fb64-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="3fb64-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3fb64-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fb64-138">OUTPUTS</span></span>

### <span data-ttu-id="3fb64-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="3fb64-139">System.Void</span></span>

## <span data-ttu-id="3fb64-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="3fb64-140">NOTES</span></span>

## <span data-ttu-id="3fb64-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fb64-141">RELATED LINKS</span></span>
