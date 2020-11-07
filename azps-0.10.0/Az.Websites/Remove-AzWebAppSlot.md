---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861869"
---
# <span data-ttu-id="80330-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="80330-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80330-102">SYNOPSIS</span></span>

## <span data-ttu-id="80330-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80330-103">SYNTAX</span></span>

### <span data-ttu-id="80330-104">S1</span><span class="sxs-lookup"><span data-stu-id="80330-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80330-105">S2</span><span class="sxs-lookup"><span data-stu-id="80330-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80330-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80330-106">DESCRIPTION</span></span>
<span data-ttu-id="80330-107">Il cmdlet **Remove-AzWebAppSlot** rimuove uno slot di Azure Web App a condizione che il gruppo di risorse e il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="80330-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="80330-108">Questo cmdlet, per impostazione predefinita, rimuove anche tutti gli slot e le metriche.</span><span class="sxs-lookup"><span data-stu-id="80330-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="80330-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80330-109">EXAMPLES</span></span>

### <span data-ttu-id="80330-110">Esempio 1: rimuovere uno slot per l'app Web</span><span class="sxs-lookup"><span data-stu-id="80330-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="80330-111">Questo comando rimuove lo slot denominato Slot001 associato al Web App ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="80330-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="80330-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80330-112">PARAMETERS</span></span>

### <span data-ttu-id="80330-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80330-113">-DefaultProfile</span></span>
<span data-ttu-id="80330-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80330-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80330-115">-Force</span><span class="sxs-lookup"><span data-stu-id="80330-115">-Force</span></span>
<span data-ttu-id="80330-116">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="80330-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="80330-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="80330-117">-Name</span></span>
<span data-ttu-id="80330-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="80330-118">WebApp Name</span></span>

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

### <span data-ttu-id="80330-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80330-119">-ResourceGroupName</span></span>
<span data-ttu-id="80330-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="80330-120">Resource Group Name</span></span>

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

### <span data-ttu-id="80330-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="80330-121">-Slot</span></span>
<span data-ttu-id="80330-122">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="80330-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="80330-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="80330-123">-WebApp</span></span>
<span data-ttu-id="80330-124">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="80330-124">WebApp Object</span></span>

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

### <span data-ttu-id="80330-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80330-125">-Confirm</span></span>
<span data-ttu-id="80330-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80330-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80330-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80330-127">-WhatIf</span></span>
<span data-ttu-id="80330-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80330-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80330-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80330-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="80330-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80330-130">-AsJob</span></span>
<span data-ttu-id="80330-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="80330-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80330-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80330-132">CommonParameters</span></span>
<span data-ttu-id="80330-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80330-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80330-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80330-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80330-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80330-135">INPUTS</span></span>

### <span data-ttu-id="80330-136">Sito</span><span class="sxs-lookup"><span data-stu-id="80330-136">Site</span></span>
<span data-ttu-id="80330-137">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="80330-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="80330-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80330-138">OUTPUTS</span></span>

### <span data-ttu-id="80330-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="80330-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="80330-140">Note</span><span class="sxs-lookup"><span data-stu-id="80330-140">NOTES</span></span>

## <span data-ttu-id="80330-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80330-141">RELATED LINKS</span></span>

[<span data-ttu-id="80330-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="80330-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="80330-144">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="80330-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="80330-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="80330-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80330-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="80330-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80330-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
