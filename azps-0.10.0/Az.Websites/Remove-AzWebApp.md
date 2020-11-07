---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861881"
---
# <span data-ttu-id="6e6a5-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6e6a5-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="6e6a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6a5-103">Rimuove un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="6e6a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e6a5-104">SYNTAX</span></span>

### <span data-ttu-id="6e6a5-105">S1</span><span class="sxs-lookup"><span data-stu-id="6e6a5-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e6a5-106">S2</span><span class="sxs-lookup"><span data-stu-id="6e6a5-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e6a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e6a5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e6a5-108">Il cmdlet **Remove-AzWebApp** rimuove un'app Azure Web, purché il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="6e6a5-109">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="6e6a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e6a5-110">EXAMPLES</span></span>

### <span data-ttu-id="6e6a5-111">Esempio 1: rimuovere un'app Web</span><span class="sxs-lookup"><span data-stu-id="6e6a5-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6e6a5-112">Questo comando rimuove l'app Azure Web denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6e6a5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e6a5-113">PARAMETERS</span></span>

### <span data-ttu-id="6e6a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6a5-114">-DefaultProfile</span></span>
<span data-ttu-id="6e6a5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e6a5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6e6a5-116">-Force</span></span>
<span data-ttu-id="6e6a5-117">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="6e6a5-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="6e6a5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e6a5-118">-Name</span></span>
<span data-ttu-id="6e6a5-119">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="6e6a5-119">WebApp Name</span></span>

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

### <span data-ttu-id="6e6a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e6a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="6e6a5-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6e6a5-121">Resource Group Name</span></span>

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

### <span data-ttu-id="6e6a5-122">-Web App</span><span class="sxs-lookup"><span data-stu-id="6e6a5-122">-WebApp</span></span>
<span data-ttu-id="6e6a5-123">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="6e6a5-123">WebApp Object</span></span>

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

### <span data-ttu-id="6e6a5-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e6a5-124">-Confirm</span></span>
<span data-ttu-id="6e6a5-125">Richiede la conferma prima di eseguire il cmdlet. Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e6a5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e6a5-126">-WhatIf</span></span>
<span data-ttu-id="6e6a5-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e6a5-128">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e6a5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e6a5-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e6a5-130">-AsJob</span></span>
<span data-ttu-id="6e6a5-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6e6a5-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e6a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6a5-132">CommonParameters</span></span>
<span data-ttu-id="6e6a5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6a5-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e6a5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6a5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e6a5-135">INPUTS</span></span>

### <span data-ttu-id="6e6a5-136">Sito</span><span class="sxs-lookup"><span data-stu-id="6e6a5-136">Site</span></span>
<span data-ttu-id="6e6a5-137">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6e6a5-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6e6a5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e6a5-138">OUTPUTS</span></span>

## <span data-ttu-id="6e6a5-139">Note</span><span class="sxs-lookup"><span data-stu-id="6e6a5-139">NOTES</span></span>

## <span data-ttu-id="6e6a5-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e6a5-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e6a5-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6e6a5-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="6e6a5-142">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6e6a5-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="6e6a5-143">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6e6a5-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="6e6a5-144">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6e6a5-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="6e6a5-145">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6e6a5-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


