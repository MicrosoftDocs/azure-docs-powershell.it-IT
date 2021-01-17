---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331960"
---
# <span data-ttu-id="708a3-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="708a3-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="708a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="708a3-102">SYNOPSIS</span></span>
<span data-ttu-id="708a3-103">New-AzWebAppContainerPSSession creerà una nuova sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="708a3-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="708a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="708a3-104">SYNTAX</span></span>

### <span data-ttu-id="708a3-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="708a3-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708a3-106">S2</span><span class="sxs-lookup"><span data-stu-id="708a3-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="708a3-107">DESCRIPTION</span></span>
<span data-ttu-id="708a3-108">New-AzWebAppContainerPSSession creerà una nuova sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="708a3-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="708a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="708a3-109">EXAMPLES</span></span>

### <span data-ttu-id="708a3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="708a3-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="708a3-111">Verrà creata una nuova sessione di PowerShell remota nell'app contenitore di Windows ContosoASP e verranno visualizzati i processi in uso nel contenitore ContosoASP</span><span class="sxs-lookup"><span data-stu-id="708a3-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="708a3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="708a3-112">PARAMETERS</span></span>

### <span data-ttu-id="708a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708a3-113">-DefaultProfile</span></span>
<span data-ttu-id="708a3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="708a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="708a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="708a3-115">-Force</span></span>
<span data-ttu-id="708a3-116">Creare la sessione di PowerShell senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="708a3-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="708a3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="708a3-117">-Name</span></span>
<span data-ttu-id="708a3-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="708a3-118">The name of the web app.</span></span>

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

### <span data-ttu-id="708a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="708a3-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="708a3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="708a3-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="708a3-121">-SlotName</span></span>
<span data-ttu-id="708a3-122">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="708a3-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="708a3-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="708a3-123">-WebApp</span></span>
<span data-ttu-id="708a3-124">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="708a3-124">The web app object</span></span>

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

### <span data-ttu-id="708a3-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="708a3-125">-Confirm</span></span>
<span data-ttu-id="708a3-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="708a3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708a3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708a3-127">-WhatIf</span></span>
<span data-ttu-id="708a3-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="708a3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="708a3-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="708a3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708a3-130">CommonParameters</span></span>
<span data-ttu-id="708a3-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708a3-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="708a3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708a3-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="708a3-133">INPUTS</span></span>

### <span data-ttu-id="708a3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="708a3-134">System.String</span></span>

### <span data-ttu-id="708a3-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="708a3-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="708a3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="708a3-136">OUTPUTS</span></span>

### <span data-ttu-id="708a3-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="708a3-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="708a3-138">Note</span><span class="sxs-lookup"><span data-stu-id="708a3-138">NOTES</span></span>

## <span data-ttu-id="708a3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="708a3-139">RELATED LINKS</span></span>
