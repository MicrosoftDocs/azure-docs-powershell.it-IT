---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521491"
---
# <span data-ttu-id="eec5e-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="eec5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eec5e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eec5e-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eec5e-103">SYNTAX</span></span>

### <span data-ttu-id="eec5e-104">S1</span><span class="sxs-lookup"><span data-stu-id="eec5e-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec5e-105">S2</span><span class="sxs-lookup"><span data-stu-id="eec5e-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec5e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eec5e-106">DESCRIPTION</span></span>
<span data-ttu-id="eec5e-107">Il cmdlet **Remove-AzureRmWebAppSlot** rimuove uno slot di Azure Web App a condizione che il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="eec5e-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="eec5e-108">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="eec5e-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="eec5e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eec5e-109">EXAMPLES</span></span>

### <span data-ttu-id="eec5e-110">Esempio 1: rimuovere uno slot per l'app Web</span><span class="sxs-lookup"><span data-stu-id="eec5e-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="eec5e-111">Questo comando rimuove lo slot denominato Slot001 associato al Web App ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="eec5e-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eec5e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eec5e-112">PARAMETERS</span></span>

### <span data-ttu-id="eec5e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="eec5e-113">-Force</span></span>
<span data-ttu-id="eec5e-114">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="eec5e-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="eec5e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="eec5e-115">-Name</span></span>
<span data-ttu-id="eec5e-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="eec5e-116">WebApp Name</span></span>

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

### <span data-ttu-id="eec5e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec5e-117">-ResourceGroupName</span></span>
<span data-ttu-id="eec5e-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="eec5e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="eec5e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="eec5e-119">-Slot</span></span>
<span data-ttu-id="eec5e-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="eec5e-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec5e-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="eec5e-121">-WebApp</span></span>
<span data-ttu-id="eec5e-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="eec5e-122">WebApp Object</span></span>

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

### <span data-ttu-id="eec5e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eec5e-123">-Confirm</span></span>
<span data-ttu-id="eec5e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eec5e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec5e-125">-WhatIf</span></span>
<span data-ttu-id="eec5e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eec5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec5e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eec5e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec5e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec5e-128">-DefaultProfile</span></span>
<span data-ttu-id="eec5e-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eec5e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec5e-130">CommonParameters</span></span>
<span data-ttu-id="eec5e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec5e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec5e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec5e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eec5e-133">INPUTS</span></span>

### <span data-ttu-id="eec5e-134">Sito</span><span class="sxs-lookup"><span data-stu-id="eec5e-134">Site</span></span>
<span data-ttu-id="eec5e-135">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="eec5e-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eec5e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eec5e-136">OUTPUTS</span></span>

### <span data-ttu-id="eec5e-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eec5e-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="eec5e-138">Note</span><span class="sxs-lookup"><span data-stu-id="eec5e-138">NOTES</span></span>

## <span data-ttu-id="eec5e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eec5e-139">RELATED LINKS</span></span>

[<span data-ttu-id="eec5e-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="eec5e-141">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="eec5e-142">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="eec5e-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="eec5e-144">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="eec5e-145">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eec5e-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="eec5e-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eec5e-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
