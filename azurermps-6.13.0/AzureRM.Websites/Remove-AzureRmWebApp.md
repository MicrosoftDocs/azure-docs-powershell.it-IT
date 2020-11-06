---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508920"
---
# <span data-ttu-id="eda48-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eda48-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="eda48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eda48-102">SYNOPSIS</span></span>
<span data-ttu-id="eda48-103">Rimuove un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="eda48-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eda48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eda48-104">SYNTAX</span></span>

### <span data-ttu-id="eda48-105">S1</span><span class="sxs-lookup"><span data-stu-id="eda48-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eda48-106">S2</span><span class="sxs-lookup"><span data-stu-id="eda48-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda48-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eda48-107">DESCRIPTION</span></span>
<span data-ttu-id="eda48-108">Il cmdlet **Remove-AzureRmWebApp** rimuove un'app Azure Web, purché il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="eda48-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="eda48-109">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="eda48-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="eda48-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eda48-110">EXAMPLES</span></span>

### <span data-ttu-id="eda48-111">Esempio 1: rimuovere un'app Web</span><span class="sxs-lookup"><span data-stu-id="eda48-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="eda48-112">Questo comando rimuove l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="eda48-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eda48-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eda48-113">PARAMETERS</span></span>

### <span data-ttu-id="eda48-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eda48-114">-AsJob</span></span>
<span data-ttu-id="eda48-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eda48-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eda48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda48-116">-DefaultProfile</span></span>
<span data-ttu-id="eda48-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eda48-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda48-118">-Force</span><span class="sxs-lookup"><span data-stu-id="eda48-118">-Force</span></span>
<span data-ttu-id="eda48-119">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="eda48-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="eda48-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eda48-120">-Name</span></span>
<span data-ttu-id="eda48-121">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="eda48-121">WebApp Name</span></span>

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

### <span data-ttu-id="eda48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda48-122">-ResourceGroupName</span></span>
<span data-ttu-id="eda48-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="eda48-123">Resource Group Name</span></span>

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

### <span data-ttu-id="eda48-124">-Web App</span><span class="sxs-lookup"><span data-stu-id="eda48-124">-WebApp</span></span>
<span data-ttu-id="eda48-125">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="eda48-125">WebApp Object</span></span>

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

### <span data-ttu-id="eda48-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eda48-126">-Confirm</span></span>
<span data-ttu-id="eda48-127">Richiede la conferma prima di eseguire il cmdlet. Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eda48-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda48-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda48-128">-WhatIf</span></span>
<span data-ttu-id="eda48-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eda48-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda48-130">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eda48-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda48-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eda48-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda48-132">CommonParameters</span></span>
<span data-ttu-id="eda48-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda48-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eda48-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda48-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eda48-135">INPUTS</span></span>

### <span data-ttu-id="eda48-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eda48-136">System.String</span></span>

### <span data-ttu-id="eda48-137">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="eda48-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="eda48-138">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eda48-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="eda48-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eda48-139">OUTPUTS</span></span>

### <span data-ttu-id="eda48-140">System. void</span><span class="sxs-lookup"><span data-stu-id="eda48-140">System.Void</span></span>

## <span data-ttu-id="eda48-141">Note</span><span class="sxs-lookup"><span data-stu-id="eda48-141">NOTES</span></span>

## <span data-ttu-id="eda48-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eda48-142">RELATED LINKS</span></span>

[<span data-ttu-id="eda48-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eda48-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="eda48-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eda48-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="eda48-145">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eda48-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="eda48-146">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eda48-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="eda48-147">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eda48-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


