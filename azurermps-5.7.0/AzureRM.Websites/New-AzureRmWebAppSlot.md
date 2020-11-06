---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: a3ae7f879827b7b260e60f0d3e0aa70e5a6ab533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512108"
---
# <span data-ttu-id="00b06-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="00b06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00b06-102">SYNOPSIS</span></span>
<span data-ttu-id="00b06-103">Crea uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="00b06-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00b06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00b06-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00b06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00b06-105">DESCRIPTION</span></span>
<span data-ttu-id="00b06-106">Il cmdlet **New-AzureRmWebAppSlot** crea uno slot di Azure Web App in un determinato gruppo di risorse che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="00b06-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="00b06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00b06-107">EXAMPLES</span></span>

### <span data-ttu-id="00b06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="00b06-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="00b06-109">Questo comando crea uno slot denominato Slot001 in un nome di app Web esistente ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="00b06-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="00b06-110">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="00b06-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="00b06-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00b06-111">PARAMETERS</span></span>

### <span data-ttu-id="00b06-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="00b06-112">-AppServicePlan</span></span>
<span data-ttu-id="00b06-113">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="00b06-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="00b06-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="00b06-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="00b06-115">Le impostazioni dell'app vengono sostituite da Hashtable</span><span class="sxs-lookup"><span data-stu-id="00b06-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="00b06-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="00b06-116">-AseName</span></span>
<span data-ttu-id="00b06-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="00b06-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="00b06-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b06-118">-AseResourceGroupName</span></span>
<span data-ttu-id="00b06-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="00b06-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="00b06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b06-120">-DefaultProfile</span></span>
<span data-ttu-id="00b06-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00b06-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b06-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="00b06-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="00b06-123">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="00b06-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="00b06-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="00b06-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="00b06-125">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="00b06-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="00b06-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="00b06-126">-Name</span></span>
<span data-ttu-id="00b06-127">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="00b06-127">Webapp Name</span></span>

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

### <span data-ttu-id="00b06-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b06-128">-ResourceGroupName</span></span>
<span data-ttu-id="00b06-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="00b06-129">Resource Group Name</span></span>

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

### <span data-ttu-id="00b06-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="00b06-130">-Slot</span></span>
<span data-ttu-id="00b06-131">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="00b06-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="00b06-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="00b06-132">-SourceWebApp</span></span>
<span data-ttu-id="00b06-133">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="00b06-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="00b06-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00b06-134">-AsJob</span></span>
<span data-ttu-id="00b06-135">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="00b06-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00b06-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b06-136">CommonParameters</span></span>
<span data-ttu-id="00b06-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b06-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b06-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b06-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b06-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00b06-139">INPUTS</span></span>

### <span data-ttu-id="00b06-140">Sito</span><span class="sxs-lookup"><span data-stu-id="00b06-140">Site</span></span>
<span data-ttu-id="00b06-141">Il parametro "SourceWebApp" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="00b06-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="00b06-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00b06-142">OUTPUTS</span></span>

## <span data-ttu-id="00b06-143">Note</span><span class="sxs-lookup"><span data-stu-id="00b06-143">NOTES</span></span>

## <span data-ttu-id="00b06-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00b06-144">RELATED LINKS</span></span>

[<span data-ttu-id="00b06-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="00b06-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="00b06-147">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="00b06-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="00b06-149">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="00b06-150">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="00b06-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="00b06-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="00b06-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="00b06-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="00b06-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
