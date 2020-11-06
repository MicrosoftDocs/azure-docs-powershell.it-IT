---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516331"
---
# <span data-ttu-id="db2e3-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="db2e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db2e3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2e3-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db2e3-103">SYNTAX</span></span>

### <span data-ttu-id="db2e3-104">S1</span><span class="sxs-lookup"><span data-stu-id="db2e3-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2e3-105">S2</span><span class="sxs-lookup"><span data-stu-id="db2e3-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2e3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db2e3-106">DESCRIPTION</span></span>
<span data-ttu-id="db2e3-107">Il cmdlet **Remove-AzureRmWebAppSlot** rimuove uno slot di Azure Web App a condizione che il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="db2e3-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="db2e3-108">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="db2e3-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="db2e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db2e3-109">EXAMPLES</span></span>

### <span data-ttu-id="db2e3-110">Esempio 1: rimuovere uno slot per l'app Web</span><span class="sxs-lookup"><span data-stu-id="db2e3-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="db2e3-111">Questo comando rimuove lo slot denominato Slot001 associato al Web App ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="db2e3-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="db2e3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db2e3-112">PARAMETERS</span></span>

### <span data-ttu-id="db2e3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db2e3-113">-AsJob</span></span>
<span data-ttu-id="db2e3-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db2e3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db2e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2e3-115">-DefaultProfile</span></span>
<span data-ttu-id="db2e3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db2e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db2e3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db2e3-117">-Force</span></span>
<span data-ttu-id="db2e3-118">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="db2e3-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="db2e3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="db2e3-119">-Name</span></span>
<span data-ttu-id="db2e3-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="db2e3-120">WebApp Name</span></span>

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

### <span data-ttu-id="db2e3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2e3-121">-ResourceGroupName</span></span>
<span data-ttu-id="db2e3-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="db2e3-122">Resource Group Name</span></span>

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

### <span data-ttu-id="db2e3-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="db2e3-123">-Slot</span></span>
<span data-ttu-id="db2e3-124">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="db2e3-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="db2e3-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="db2e3-125">-WebApp</span></span>
<span data-ttu-id="db2e3-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="db2e3-126">WebApp Object</span></span>

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

### <span data-ttu-id="db2e3-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db2e3-127">-Confirm</span></span>
<span data-ttu-id="db2e3-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2e3-129">-WhatIf</span></span>
<span data-ttu-id="db2e3-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db2e3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2e3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db2e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2e3-132">CommonParameters</span></span>
<span data-ttu-id="db2e3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2e3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2e3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2e3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db2e3-135">INPUTS</span></span>

### <span data-ttu-id="db2e3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="db2e3-136">System.String</span></span>

### <span data-ttu-id="db2e3-137">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="db2e3-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="db2e3-138">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db2e3-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="db2e3-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db2e3-139">OUTPUTS</span></span>

### <span data-ttu-id="db2e3-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="db2e3-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="db2e3-141">Note</span><span class="sxs-lookup"><span data-stu-id="db2e3-141">NOTES</span></span>

## <span data-ttu-id="db2e3-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db2e3-142">RELATED LINKS</span></span>

[<span data-ttu-id="db2e3-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="db2e3-144">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="db2e3-145">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="db2e3-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="db2e3-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="db2e3-148">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db2e3-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="db2e3-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="db2e3-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
