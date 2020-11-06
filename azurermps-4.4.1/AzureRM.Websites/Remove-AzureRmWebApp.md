---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521494"
---
# <span data-ttu-id="eca32-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca32-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="eca32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eca32-102">SYNOPSIS</span></span>
<span data-ttu-id="eca32-103">Rimuove un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="eca32-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eca32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eca32-104">SYNTAX</span></span>

### <span data-ttu-id="eca32-105">S1</span><span class="sxs-lookup"><span data-stu-id="eca32-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca32-106">S2</span><span class="sxs-lookup"><span data-stu-id="eca32-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eca32-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eca32-107">DESCRIPTION</span></span>
<span data-ttu-id="eca32-108">Il cmdlet **Remove-AzureRmWebApp** rimuove un'app Azure Web, purché il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="eca32-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="eca32-109">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="eca32-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="eca32-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eca32-110">EXAMPLES</span></span>

### <span data-ttu-id="eca32-111">Esempio 1: rimuovere un'app Web</span><span class="sxs-lookup"><span data-stu-id="eca32-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="eca32-112">Questo comando rimuove l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="eca32-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eca32-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eca32-113">PARAMETERS</span></span>

### <span data-ttu-id="eca32-114">-Force</span><span class="sxs-lookup"><span data-stu-id="eca32-114">-Force</span></span>
<span data-ttu-id="eca32-115">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="eca32-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="eca32-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eca32-116">-Name</span></span>
<span data-ttu-id="eca32-117">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="eca32-117">WebApp Name</span></span>

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

### <span data-ttu-id="eca32-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca32-118">-ResourceGroupName</span></span>
<span data-ttu-id="eca32-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="eca32-119">Resource Group Name</span></span>

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

### <span data-ttu-id="eca32-120">-Web App</span><span class="sxs-lookup"><span data-stu-id="eca32-120">-WebApp</span></span>
<span data-ttu-id="eca32-121">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="eca32-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eca32-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eca32-122">-Confirm</span></span>
<span data-ttu-id="eca32-123">Richiede la conferma prima di eseguire il cmdlet. Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca32-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca32-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca32-124">-WhatIf</span></span>
<span data-ttu-id="eca32-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eca32-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca32-126">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eca32-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca32-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eca32-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca32-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca32-128">-DefaultProfile</span></span>
<span data-ttu-id="eca32-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eca32-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eca32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca32-130">CommonParameters</span></span>
<span data-ttu-id="eca32-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca32-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca32-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca32-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eca32-133">INPUTS</span></span>

### <span data-ttu-id="eca32-134">Sito</span><span class="sxs-lookup"><span data-stu-id="eca32-134">Site</span></span>
<span data-ttu-id="eca32-135">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="eca32-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eca32-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eca32-136">OUTPUTS</span></span>

## <span data-ttu-id="eca32-137">Note</span><span class="sxs-lookup"><span data-stu-id="eca32-137">NOTES</span></span>

## <span data-ttu-id="eca32-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eca32-138">RELATED LINKS</span></span>

[<span data-ttu-id="eca32-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca32-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="eca32-140">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca32-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="eca32-141">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca32-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="eca32-142">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca32-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="eca32-143">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca32-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


