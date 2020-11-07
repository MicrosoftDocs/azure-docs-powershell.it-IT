---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865987"
---
# <span data-ttu-id="36675-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="36675-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="36675-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36675-102">SYNOPSIS</span></span>
<span data-ttu-id="36675-103">Ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="36675-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36675-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36675-104">SYNTAX</span></span>

### <span data-ttu-id="36675-105">S1</span><span class="sxs-lookup"><span data-stu-id="36675-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36675-106">S2</span><span class="sxs-lookup"><span data-stu-id="36675-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36675-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36675-107">DESCRIPTION</span></span>
<span data-ttu-id="36675-108">Il cmdlet **Get-AzureRmWebAppPublishingProfile** ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="36675-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="36675-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36675-109">EXAMPLES</span></span>

### <span data-ttu-id="36675-110">1:</span><span class="sxs-lookup"><span data-stu-id="36675-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="36675-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="36675-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="36675-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36675-112">PARAMETERS</span></span>

### <span data-ttu-id="36675-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36675-113">-DefaultProfile</span></span>
<span data-ttu-id="36675-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36675-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36675-115">-Format</span><span class="sxs-lookup"><span data-stu-id="36675-115">-Format</span></span>
<span data-ttu-id="36675-116">Formato</span><span class="sxs-lookup"><span data-stu-id="36675-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36675-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="36675-117">-Name</span></span>
<span data-ttu-id="36675-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="36675-118">WebApp Name</span></span>

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

### <span data-ttu-id="36675-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="36675-119">-OutputFile</span></span>
<span data-ttu-id="36675-120">File di output</span><span class="sxs-lookup"><span data-stu-id="36675-120">Output File</span></span>

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

### <span data-ttu-id="36675-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36675-121">-ResourceGroupName</span></span>
<span data-ttu-id="36675-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="36675-122">Resource Group Name</span></span>

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

### <span data-ttu-id="36675-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="36675-123">-WebApp</span></span>
<span data-ttu-id="36675-124">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="36675-124">WebApp Object</span></span>

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

### <span data-ttu-id="36675-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36675-125">CommonParameters</span></span>
<span data-ttu-id="36675-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36675-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36675-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36675-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36675-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36675-128">INPUTS</span></span>

### <span data-ttu-id="36675-129">Sito</span><span class="sxs-lookup"><span data-stu-id="36675-129">Site</span></span>
<span data-ttu-id="36675-130">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="36675-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="36675-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36675-131">OUTPUTS</span></span>

## <span data-ttu-id="36675-132">Note</span><span class="sxs-lookup"><span data-stu-id="36675-132">NOTES</span></span>

## <span data-ttu-id="36675-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36675-133">RELATED LINKS</span></span>

[<span data-ttu-id="36675-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="36675-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="36675-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="36675-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


