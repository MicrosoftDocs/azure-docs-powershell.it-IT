---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 213fbd5e035c48892db1c44fb4ac8de8fbf8bba9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967118"
---
# <span data-ttu-id="c0598-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="c0598-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="c0598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0598-102">SYNOPSIS</span></span>
<span data-ttu-id="c0598-103">New-AzWebAppContainerPSSession crea una nuova sessione remota di PowerShell nel contenitore di windows specificato in un determinato sito o slot e gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c0598-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="c0598-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0598-104">SYNTAX</span></span>

### <span data-ttu-id="c0598-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0598-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0598-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0598-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0598-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0598-107">DESCRIPTION</span></span>
<span data-ttu-id="c0598-108">New-AzWebAppContainerPSSession crea una nuova sessione remota di PowerShell nel contenitore di windows specificato in un determinato sito o slot e gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c0598-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="c0598-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0598-109">EXAMPLES</span></span>

### <span data-ttu-id="c0598-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0598-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="c0598-111">Verrà creata una nuova sessione di PowerShell remota nell'app contenitore di Windows ContosoASP e verranno visualizzati i processi in esecuzione nel contenitore ContosoASP</span><span class="sxs-lookup"><span data-stu-id="c0598-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="c0598-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0598-112">PARAMETERS</span></span>

### <span data-ttu-id="c0598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0598-113">-DefaultProfile</span></span>
<span data-ttu-id="c0598-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0598-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0598-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0598-115">-Force</span></span>
<span data-ttu-id="c0598-116">Creare la sessione di PowerShell senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c0598-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c0598-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c0598-117">-Name</span></span>
<span data-ttu-id="c0598-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="c0598-118">The name of the web app.</span></span>

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

### <span data-ttu-id="c0598-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0598-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0598-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0598-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0598-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="c0598-121">-SlotName</span></span>
<span data-ttu-id="c0598-122">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="c0598-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="c0598-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c0598-123">-WebApp</span></span>
<span data-ttu-id="c0598-124">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="c0598-124">The web app object</span></span>

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

### <span data-ttu-id="c0598-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0598-125">-Confirm</span></span>
<span data-ttu-id="c0598-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0598-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0598-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0598-127">-WhatIf</span></span>
<span data-ttu-id="c0598-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0598-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0598-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0598-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0598-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0598-130">CommonParameters</span></span>
<span data-ttu-id="c0598-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0598-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0598-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0598-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0598-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0598-133">INPUTS</span></span>

### <span data-ttu-id="c0598-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c0598-134">System.String</span></span>

### <span data-ttu-id="c0598-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c0598-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c0598-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0598-136">OUTPUTS</span></span>

### <span data-ttu-id="c0598-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="c0598-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="c0598-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0598-138">NOTES</span></span>

## <span data-ttu-id="c0598-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0598-139">RELATED LINKS</span></span>
