---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: c91e5ff71a916e28e199a1c64fde2d69f0193fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676279"
---
# <span data-ttu-id="d4d78-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4d78-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="d4d78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4d78-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d78-103">Rimuove un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="d4d78-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="d4d78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4d78-104">SYNTAX</span></span>

### <span data-ttu-id="d4d78-105">S1</span><span class="sxs-lookup"><span data-stu-id="d4d78-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d78-106">S2</span><span class="sxs-lookup"><span data-stu-id="d4d78-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4d78-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4d78-107">DESCRIPTION</span></span>
<span data-ttu-id="d4d78-108">Il cmdlet **Remove-AzWebApp** rimuove un'app Azure Web, purché il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="d4d78-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="d4d78-109">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="d4d78-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d4d78-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4d78-110">EXAMPLES</span></span>

### <span data-ttu-id="d4d78-111">Esempio 1: rimuovere un'app Web</span><span class="sxs-lookup"><span data-stu-id="d4d78-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d4d78-112">Questo comando rimuove l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="d4d78-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d4d78-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4d78-113">PARAMETERS</span></span>

### <span data-ttu-id="d4d78-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4d78-114">-AsJob</span></span>
<span data-ttu-id="d4d78-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d4d78-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4d78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d78-116">-DefaultProfile</span></span>
<span data-ttu-id="d4d78-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d78-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4d78-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d4d78-118">-Force</span></span>
<span data-ttu-id="d4d78-119">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="d4d78-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d4d78-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4d78-120">-Name</span></span>
<span data-ttu-id="d4d78-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="d4d78-121">WebApp Name</span></span>

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

### <span data-ttu-id="d4d78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d78-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4d78-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d4d78-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d4d78-124">-Web App</span><span class="sxs-lookup"><span data-stu-id="d4d78-124">-WebApp</span></span>
<span data-ttu-id="d4d78-125">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="d4d78-125">WebApp Object</span></span>

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

### <span data-ttu-id="d4d78-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4d78-126">-Confirm</span></span>
<span data-ttu-id="d4d78-127">Richiede la conferma prima di eseguire il cmdlet. Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4d78-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d78-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d78-128">-WhatIf</span></span>
<span data-ttu-id="d4d78-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4d78-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d78-130">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4d78-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d78-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4d78-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d78-132">CommonParameters</span></span>
<span data-ttu-id="d4d78-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d78-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d78-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4d78-135">INPUTS</span></span>

### <span data-ttu-id="d4d78-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d78-136">System.String</span></span>

### <span data-ttu-id="d4d78-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d4d78-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d4d78-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4d78-138">OUTPUTS</span></span>

### <span data-ttu-id="d4d78-139">System. void</span><span class="sxs-lookup"><span data-stu-id="d4d78-139">System.Void</span></span>

## <span data-ttu-id="d4d78-140">Note</span><span class="sxs-lookup"><span data-stu-id="d4d78-140">NOTES</span></span>

## <span data-ttu-id="d4d78-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4d78-141">RELATED LINKS</span></span>

[<span data-ttu-id="d4d78-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4d78-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d4d78-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4d78-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d4d78-144">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4d78-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d4d78-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4d78-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d4d78-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4d78-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


