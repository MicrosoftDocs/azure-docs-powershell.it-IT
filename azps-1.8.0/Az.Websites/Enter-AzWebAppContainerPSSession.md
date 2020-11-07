---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: b18008268ffd07369cf527c53d6ad693a38d85f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676335"
---
# <span data-ttu-id="5789b-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="5789b-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="5789b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5789b-102">SYNOPSIS</span></span>
<span data-ttu-id="5789b-103">Apre una sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5789b-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="5789b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5789b-104">SYNTAX</span></span>

### <span data-ttu-id="5789b-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5789b-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5789b-106">S2</span><span class="sxs-lookup"><span data-stu-id="5789b-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5789b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5789b-107">DESCRIPTION</span></span>
<span data-ttu-id="5789b-108">apre una sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5789b-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="5789b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5789b-109">EXAMPLES</span></span>

### <span data-ttu-id="5789b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5789b-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="5789b-111">Questo comando apre una sessione remota di PowerShell nell'app contenitore di Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="5789b-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="5789b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5789b-112">PARAMETERS</span></span>

### <span data-ttu-id="5789b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5789b-113">-DefaultProfile</span></span>
<span data-ttu-id="5789b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5789b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5789b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5789b-115">-Force</span></span>
<span data-ttu-id="5789b-116">Creare la sessione di PowerShell senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5789b-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5789b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5789b-117">-Name</span></span>
<span data-ttu-id="5789b-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="5789b-118">The name of the web app.</span></span>

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

### <span data-ttu-id="5789b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5789b-119">-PassThru</span></span>
<span data-ttu-id="5789b-120">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="5789b-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="5789b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5789b-121">-ResourceGroupName</span></span>
<span data-ttu-id="5789b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5789b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5789b-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="5789b-123">-SlotName</span></span>
<span data-ttu-id="5789b-124">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="5789b-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="5789b-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="5789b-125">-WebApp</span></span>
<span data-ttu-id="5789b-126">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="5789b-126">The web app object</span></span>

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

### <span data-ttu-id="5789b-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5789b-127">-Confirm</span></span>
<span data-ttu-id="5789b-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5789b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5789b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5789b-129">-WhatIf</span></span>
<span data-ttu-id="5789b-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5789b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5789b-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5789b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5789b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5789b-132">CommonParameters</span></span>
<span data-ttu-id="5789b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5789b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5789b-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5789b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5789b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5789b-135">INPUTS</span></span>

### <span data-ttu-id="5789b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5789b-136">System.String</span></span>

### <span data-ttu-id="5789b-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5789b-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5789b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5789b-138">OUTPUTS</span></span>

### <span data-ttu-id="5789b-139">System. void</span><span class="sxs-lookup"><span data-stu-id="5789b-139">System.Void</span></span>

## <span data-ttu-id="5789b-140">Note</span><span class="sxs-lookup"><span data-stu-id="5789b-140">NOTES</span></span>

## <span data-ttu-id="5789b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5789b-141">RELATED LINKS</span></span>