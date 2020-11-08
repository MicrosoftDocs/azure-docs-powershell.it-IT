---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202712"
---
# <span data-ttu-id="e3b80-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="e3b80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3b80-102">SYNOPSIS</span></span>

## <span data-ttu-id="e3b80-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3b80-103">SYNTAX</span></span>

### <span data-ttu-id="e3b80-104">S1</span><span class="sxs-lookup"><span data-stu-id="e3b80-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b80-105">S2</span><span class="sxs-lookup"><span data-stu-id="e3b80-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b80-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3b80-106">DESCRIPTION</span></span>
<span data-ttu-id="e3b80-107">Il cmdlet **Remove-AzWebAppSlot** rimuove uno slot di Azure Web App a condizione che il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="e3b80-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="e3b80-108">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="e3b80-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="e3b80-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3b80-109">EXAMPLES</span></span>

### <span data-ttu-id="e3b80-110">Esempio 1: rimuovere uno slot per l'app Web</span><span class="sxs-lookup"><span data-stu-id="e3b80-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="e3b80-111">Questo comando rimuove lo slot denominato Slot001 associato al Web App ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="e3b80-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e3b80-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3b80-112">PARAMETERS</span></span>

### <span data-ttu-id="e3b80-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3b80-113">-AsJob</span></span>
<span data-ttu-id="e3b80-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3b80-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3b80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b80-115">-DefaultProfile</span></span>
<span data-ttu-id="e3b80-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b80-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b80-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e3b80-117">-Force</span></span>
<span data-ttu-id="e3b80-118">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="e3b80-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e3b80-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3b80-119">-Name</span></span>
<span data-ttu-id="e3b80-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="e3b80-120">WebApp Name</span></span>

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

### <span data-ttu-id="e3b80-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b80-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3b80-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e3b80-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e3b80-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3b80-123">-Slot</span></span>
<span data-ttu-id="e3b80-124">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="e3b80-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e3b80-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="e3b80-125">-WebApp</span></span>
<span data-ttu-id="e3b80-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="e3b80-126">WebApp Object</span></span>

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

### <span data-ttu-id="e3b80-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3b80-127">-Confirm</span></span>
<span data-ttu-id="e3b80-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b80-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b80-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b80-129">-WhatIf</span></span>
<span data-ttu-id="e3b80-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3b80-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b80-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3b80-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b80-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b80-132">CommonParameters</span></span>
<span data-ttu-id="e3b80-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b80-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b80-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b80-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b80-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3b80-135">INPUTS</span></span>

### <span data-ttu-id="e3b80-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b80-136">System.String</span></span>

### <span data-ttu-id="e3b80-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e3b80-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e3b80-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3b80-138">OUTPUTS</span></span>

### <span data-ttu-id="e3b80-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3b80-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e3b80-140">Note</span><span class="sxs-lookup"><span data-stu-id="e3b80-140">NOTES</span></span>

## <span data-ttu-id="e3b80-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3b80-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3b80-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e3b80-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="e3b80-144">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="e3b80-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="e3b80-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="e3b80-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3b80-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="e3b80-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3b80-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
