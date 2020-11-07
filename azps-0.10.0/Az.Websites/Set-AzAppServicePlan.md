---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861834"
---
# <span data-ttu-id="8ae6b-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ae6b-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="8ae6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ae6b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae6b-103">Imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="8ae6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ae6b-104">SYNTAX</span></span>

### <span data-ttu-id="8ae6b-105">S1</span><span class="sxs-lookup"><span data-stu-id="8ae6b-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ae6b-106">S2</span><span class="sxs-lookup"><span data-stu-id="8ae6b-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ae6b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ae6b-107">DESCRIPTION</span></span>
<span data-ttu-id="8ae6b-108">Il cmdlet **set-AzAppServicePlan** imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="8ae6b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ae6b-109">EXAMPLES</span></span>

### <span data-ttu-id="8ae6b-110">1: modificare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="8ae6b-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="8ae6b-111">Questo comando imposta l'opzione PerSiteScaling su true nel piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8ae6b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ae6b-112">PARAMETERS</span></span>

### <span data-ttu-id="8ae6b-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="8ae6b-113">-AdminSiteName</span></span>
<span data-ttu-id="8ae6b-114">Nome sito amministratore</span><span class="sxs-lookup"><span data-stu-id="8ae6b-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae6b-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ae6b-115">-AppServicePlan</span></span>
<span data-ttu-id="8ae6b-116">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="8ae6b-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae6b-117">-DefaultProfile</span></span>
<span data-ttu-id="8ae6b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ae6b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ae6b-119">-Name</span></span>
<span data-ttu-id="8ae6b-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="8ae6b-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae6b-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="8ae6b-121">-NumberofWorkers</span></span>
<span data-ttu-id="8ae6b-122">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="8ae6b-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae6b-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="8ae6b-123">-PerSiteScaling</span></span>
<span data-ttu-id="8ae6b-124">Booleano scala per sito</span><span class="sxs-lookup"><span data-stu-id="8ae6b-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae6b-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ae6b-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8ae6b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8ae6b-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="8ae6b-127">-Tier</span></span>
<span data-ttu-id="8ae6b-128">Livello</span><span class="sxs-lookup"><span data-stu-id="8ae6b-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae6b-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="8ae6b-129">-WorkerSize</span></span>
<span data-ttu-id="8ae6b-130">Dimensioni lavoratore</span><span class="sxs-lookup"><span data-stu-id="8ae6b-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="8ae6b-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae6b-131">-AsJob</span></span>
<span data-ttu-id="8ae6b-132">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8ae6b-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ae6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae6b-133">CommonParameters</span></span>
<span data-ttu-id="8ae6b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae6b-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae6b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae6b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ae6b-136">INPUTS</span></span>

### <span data-ttu-id="8ae6b-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8ae6b-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="8ae6b-138">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8ae6b-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="8ae6b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ae6b-139">OUTPUTS</span></span>

### <span data-ttu-id="8ae6b-140">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8ae6b-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="8ae6b-141">Note</span><span class="sxs-lookup"><span data-stu-id="8ae6b-141">NOTES</span></span>

## <span data-ttu-id="8ae6b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ae6b-142">RELATED LINKS</span></span>

[<span data-ttu-id="8ae6b-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ae6b-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8ae6b-144">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ae6b-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8ae6b-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ae6b-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8ae6b-146">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ae6b-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8ae6b-147">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ae6b-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8ae6b-148">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ae6b-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


