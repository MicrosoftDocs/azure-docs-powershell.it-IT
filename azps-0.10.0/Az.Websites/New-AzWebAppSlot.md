---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861873"
---
# <span data-ttu-id="60feb-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="60feb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60feb-102">SYNOPSIS</span></span>
<span data-ttu-id="60feb-103">Crea uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="60feb-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="60feb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60feb-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60feb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60feb-105">DESCRIPTION</span></span>
<span data-ttu-id="60feb-106">Il cmdlet **New-AzWebAppSlot** crea uno slot di Azure Web App in un determinato gruppo di risorse che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="60feb-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="60feb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60feb-107">EXAMPLES</span></span>

### <span data-ttu-id="60feb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60feb-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="60feb-109">Questo comando crea uno slot denominato Slot001 in un nome di app Web esistente ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="60feb-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="60feb-110">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="60feb-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="60feb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60feb-111">PARAMETERS</span></span>

### <span data-ttu-id="60feb-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="60feb-112">-AppServicePlan</span></span>
<span data-ttu-id="60feb-113">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="60feb-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="60feb-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="60feb-115">Le impostazioni dell'app vengono sostituite da Hashtable</span><span class="sxs-lookup"><span data-stu-id="60feb-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="60feb-116">-AseName</span></span>
<span data-ttu-id="60feb-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="60feb-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60feb-118">-AseResourceGroupName</span></span>
<span data-ttu-id="60feb-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="60feb-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60feb-120">-DefaultProfile</span></span>
<span data-ttu-id="60feb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60feb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60feb-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="60feb-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="60feb-123">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="60feb-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="60feb-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="60feb-125">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="60feb-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="60feb-126">-Name</span></span>
<span data-ttu-id="60feb-127">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="60feb-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60feb-128">-ResourceGroupName</span></span>
<span data-ttu-id="60feb-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="60feb-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="60feb-130">-Slot</span></span>
<span data-ttu-id="60feb-131">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="60feb-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="60feb-132">-SourceWebApp</span></span>
<span data-ttu-id="60feb-133">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="60feb-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60feb-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60feb-134">-AsJob</span></span>
<span data-ttu-id="60feb-135">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60feb-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60feb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60feb-136">CommonParameters</span></span>
<span data-ttu-id="60feb-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60feb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60feb-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60feb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60feb-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60feb-139">INPUTS</span></span>

### <span data-ttu-id="60feb-140">Sito</span><span class="sxs-lookup"><span data-stu-id="60feb-140">Site</span></span>
<span data-ttu-id="60feb-141">Il parametro "SourceWebApp" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="60feb-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="60feb-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60feb-142">OUTPUTS</span></span>

## <span data-ttu-id="60feb-143">Note</span><span class="sxs-lookup"><span data-stu-id="60feb-143">NOTES</span></span>

## <span data-ttu-id="60feb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60feb-144">RELATED LINKS</span></span>

[<span data-ttu-id="60feb-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="60feb-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="60feb-147">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="60feb-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="60feb-149">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="60feb-150">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60feb-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="60feb-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="60feb-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="60feb-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60feb-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
