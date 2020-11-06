---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508924"
---
# <span data-ttu-id="d2221-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="d2221-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="d2221-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2221-102">SYNOPSIS</span></span>
<span data-ttu-id="d2221-103">New-AzureRmWebAppContainerPSSession creerà una nuova sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d2221-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2221-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2221-104">SYNTAX</span></span>

### <span data-ttu-id="d2221-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2221-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2221-106">S2</span><span class="sxs-lookup"><span data-stu-id="d2221-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2221-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2221-107">DESCRIPTION</span></span>
<span data-ttu-id="d2221-108">New-AzureRmWebAppContainerPSSession creerà una nuova sessione remota di PowerShell nel contenitore di Windows specificato in un determinato sito o uno slot e un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d2221-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="d2221-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2221-109">EXAMPLES</span></span>

### <span data-ttu-id="d2221-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2221-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="d2221-111">Verrà creata una nuova sessione di PowerShell remota nell'app contenitore di Windows ContosoASP e verranno visualizzati i processi in uso nel contenitore ContosoASP</span><span class="sxs-lookup"><span data-stu-id="d2221-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="d2221-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2221-112">PARAMETERS</span></span>

### <span data-ttu-id="d2221-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2221-113">-DefaultProfile</span></span>
<span data-ttu-id="d2221-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2221-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2221-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d2221-115">-Force</span></span>
<span data-ttu-id="d2221-116">Creare la sessione di PowerShell senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d2221-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d2221-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2221-117">-Name</span></span>
<span data-ttu-id="d2221-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="d2221-118">The name of the web app.</span></span>

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

### <span data-ttu-id="d2221-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2221-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2221-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2221-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="d2221-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="d2221-121">-SlotName</span></span>
<span data-ttu-id="d2221-122">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="d2221-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="d2221-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="d2221-123">-WebApp</span></span>
<span data-ttu-id="d2221-124">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="d2221-124">The web app object</span></span>

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

### <span data-ttu-id="d2221-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2221-125">-Confirm</span></span>
<span data-ttu-id="d2221-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2221-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2221-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2221-127">-WhatIf</span></span>
<span data-ttu-id="d2221-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2221-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2221-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2221-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2221-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2221-130">CommonParameters</span></span>
<span data-ttu-id="d2221-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2221-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2221-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2221-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2221-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2221-133">INPUTS</span></span>

### <span data-ttu-id="d2221-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d2221-134">System.String</span></span>
### <span data-ttu-id="d2221-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d2221-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="d2221-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2221-136">OUTPUTS</span></span>

### <span data-ttu-id="d2221-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d2221-137">System.String</span></span>
## <span data-ttu-id="d2221-138">Note</span><span class="sxs-lookup"><span data-stu-id="d2221-138">NOTES</span></span>

## <span data-ttu-id="d2221-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2221-139">RELATED LINKS</span></span>
