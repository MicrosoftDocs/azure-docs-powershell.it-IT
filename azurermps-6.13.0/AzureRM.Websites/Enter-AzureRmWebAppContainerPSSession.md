---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508932"
---
# <span data-ttu-id="b29d5-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="b29d5-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="b29d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b29d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b29d5-103">Apre una sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b29d5-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b29d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b29d5-104">SYNTAX</span></span>

### <span data-ttu-id="b29d5-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b29d5-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b29d5-106">S2</span><span class="sxs-lookup"><span data-stu-id="b29d5-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b29d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b29d5-107">DESCRIPTION</span></span>
<span data-ttu-id="b29d5-108">apre una sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b29d5-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b29d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b29d5-109">EXAMPLES</span></span>

### <span data-ttu-id="b29d5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b29d5-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b29d5-111">Questo comando apre una sessione remota di PowerShell nell'app contenitore di Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="b29d5-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="b29d5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b29d5-112">PARAMETERS</span></span>

### <span data-ttu-id="b29d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29d5-113">-DefaultProfile</span></span>
<span data-ttu-id="b29d5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b29d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29d5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b29d5-115">-Force</span></span>
<span data-ttu-id="b29d5-116">Creare la sessione di PowerShell senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b29d5-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b29d5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b29d5-117">-Name</span></span>
<span data-ttu-id="b29d5-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="b29d5-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b29d5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b29d5-119">-PassThru</span></span>
<span data-ttu-id="b29d5-120">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="b29d5-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="b29d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="b29d5-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b29d5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b29d5-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="b29d5-123">-SlotName</span></span>
<span data-ttu-id="b29d5-124">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="b29d5-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b29d5-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="b29d5-125">-WebApp</span></span>
<span data-ttu-id="b29d5-126">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="b29d5-126">The web app object</span></span>

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

### <span data-ttu-id="b29d5-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b29d5-127">-Confirm</span></span>
<span data-ttu-id="b29d5-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b29d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b29d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b29d5-129">-WhatIf</span></span>
<span data-ttu-id="b29d5-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b29d5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b29d5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b29d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b29d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29d5-132">CommonParameters</span></span>
<span data-ttu-id="b29d5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29d5-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29d5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b29d5-135">INPUTS</span></span>

### <span data-ttu-id="b29d5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b29d5-136">System.String</span></span>
### <span data-ttu-id="b29d5-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b29d5-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="b29d5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b29d5-138">OUTPUTS</span></span>

### <span data-ttu-id="b29d5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b29d5-139">System.String</span></span>
## <span data-ttu-id="b29d5-140">Note</span><span class="sxs-lookup"><span data-stu-id="b29d5-140">NOTES</span></span>

## <span data-ttu-id="b29d5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b29d5-141">RELATED LINKS</span></span>
