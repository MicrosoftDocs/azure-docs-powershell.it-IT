---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520318"
---
# <span data-ttu-id="21332-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="21332-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21332-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21332-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21332-103">SYNTAX</span></span>

### <span data-ttu-id="21332-104">S1</span><span class="sxs-lookup"><span data-stu-id="21332-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21332-105">S2</span><span class="sxs-lookup"><span data-stu-id="21332-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21332-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21332-106">DESCRIPTION</span></span>
<span data-ttu-id="21332-107">Il cmdlet **Remove-AzureRmWebAppSlot** rimuove uno slot di Azure Web App a condizione che il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="21332-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="21332-108">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="21332-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="21332-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21332-109">EXAMPLES</span></span>

### <span data-ttu-id="21332-110">Esempio 1: rimuovere uno slot per l'app Web</span><span class="sxs-lookup"><span data-stu-id="21332-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="21332-111">Questo comando rimuove lo slot denominato Slot001 associato al Web App ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="21332-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="21332-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21332-112">PARAMETERS</span></span>

### <span data-ttu-id="21332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21332-113">-DefaultProfile</span></span>
<span data-ttu-id="21332-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21332-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21332-115">-Force</span><span class="sxs-lookup"><span data-stu-id="21332-115">-Force</span></span>
<span data-ttu-id="21332-116">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="21332-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="21332-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="21332-117">-Name</span></span>
<span data-ttu-id="21332-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="21332-118">WebApp Name</span></span>

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

### <span data-ttu-id="21332-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21332-119">-ResourceGroupName</span></span>
<span data-ttu-id="21332-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="21332-120">Resource Group Name</span></span>

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

### <span data-ttu-id="21332-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="21332-121">-Slot</span></span>
<span data-ttu-id="21332-122">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="21332-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21332-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="21332-123">-WebApp</span></span>
<span data-ttu-id="21332-124">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="21332-124">WebApp Object</span></span>

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

### <span data-ttu-id="21332-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21332-125">-Confirm</span></span>
<span data-ttu-id="21332-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21332-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21332-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21332-127">-WhatIf</span></span>
<span data-ttu-id="21332-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21332-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21332-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21332-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="21332-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21332-130">-AsJob</span></span>
<span data-ttu-id="21332-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="21332-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21332-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21332-132">CommonParameters</span></span>
<span data-ttu-id="21332-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21332-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21332-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21332-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21332-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21332-135">INPUTS</span></span>

### <span data-ttu-id="21332-136">Sito</span><span class="sxs-lookup"><span data-stu-id="21332-136">Site</span></span>
<span data-ttu-id="21332-137">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="21332-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="21332-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21332-138">OUTPUTS</span></span>

### <span data-ttu-id="21332-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="21332-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="21332-140">Note</span><span class="sxs-lookup"><span data-stu-id="21332-140">NOTES</span></span>

## <span data-ttu-id="21332-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21332-141">RELATED LINKS</span></span>

[<span data-ttu-id="21332-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="21332-143">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="21332-144">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="21332-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="21332-146">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="21332-147">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21332-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="21332-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21332-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
