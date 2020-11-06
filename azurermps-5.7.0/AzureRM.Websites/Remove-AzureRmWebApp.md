---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: a984a9a76a41db93bee96acfa029ca05a30d85f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512119"
---
# <span data-ttu-id="f8806-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8806-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="f8806-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8806-102">SYNOPSIS</span></span>
<span data-ttu-id="f8806-103">Rimuove un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="f8806-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8806-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8806-104">SYNTAX</span></span>

### <span data-ttu-id="f8806-105">S1</span><span class="sxs-lookup"><span data-stu-id="f8806-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8806-106">S2</span><span class="sxs-lookup"><span data-stu-id="f8806-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8806-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8806-107">DESCRIPTION</span></span>
<span data-ttu-id="f8806-108">Il cmdlet **Remove-AzureRmWebApp** rimuove un'app Azure Web, purché il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="f8806-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="f8806-109">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="f8806-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="f8806-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8806-110">EXAMPLES</span></span>

### <span data-ttu-id="f8806-111">Esempio 1: rimuovere un'app Web</span><span class="sxs-lookup"><span data-stu-id="f8806-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f8806-112">Questo comando rimuove l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="f8806-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f8806-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8806-113">PARAMETERS</span></span>

### <span data-ttu-id="f8806-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8806-114">-DefaultProfile</span></span>
<span data-ttu-id="f8806-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8806-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8806-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f8806-116">-Force</span></span>
<span data-ttu-id="f8806-117">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="f8806-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="f8806-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8806-118">-Name</span></span>
<span data-ttu-id="f8806-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="f8806-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8806-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8806-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8806-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f8806-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8806-122">-Web App</span><span class="sxs-lookup"><span data-stu-id="f8806-122">-WebApp</span></span>
<span data-ttu-id="f8806-123">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="f8806-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8806-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8806-124">-Confirm</span></span>
<span data-ttu-id="f8806-125">Richiede la conferma prima di eseguire il cmdlet. Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8806-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8806-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8806-126">-WhatIf</span></span>
<span data-ttu-id="f8806-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8806-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8806-128">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8806-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8806-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8806-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8806-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8806-130">-AsJob</span></span>
<span data-ttu-id="f8806-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f8806-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8806-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8806-132">CommonParameters</span></span>
<span data-ttu-id="f8806-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8806-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8806-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8806-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8806-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8806-135">INPUTS</span></span>

### <span data-ttu-id="f8806-136">Sito</span><span class="sxs-lookup"><span data-stu-id="f8806-136">Site</span></span>
<span data-ttu-id="f8806-137">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f8806-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f8806-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8806-138">OUTPUTS</span></span>

## <span data-ttu-id="f8806-139">Note</span><span class="sxs-lookup"><span data-stu-id="f8806-139">NOTES</span></span>

## <span data-ttu-id="f8806-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8806-140">RELATED LINKS</span></span>

[<span data-ttu-id="f8806-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8806-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f8806-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8806-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f8806-143">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8806-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f8806-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8806-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f8806-145">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8806-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


