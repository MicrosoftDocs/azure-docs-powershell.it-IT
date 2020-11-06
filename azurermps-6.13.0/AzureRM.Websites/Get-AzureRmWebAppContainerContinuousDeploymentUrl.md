---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514727"
---
# <span data-ttu-id="09af1-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="09af1-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="09af1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09af1-102">SYNOPSIS</span></span>
<span data-ttu-id="09af1-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="09af1-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09af1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09af1-104">SYNTAX</span></span>

### <span data-ttu-id="09af1-105">S1</span><span class="sxs-lookup"><span data-stu-id="09af1-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09af1-106">S2</span><span class="sxs-lookup"><span data-stu-id="09af1-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09af1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09af1-107">DESCRIPTION</span></span>
<span data-ttu-id="09af1-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="09af1-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="09af1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09af1-109">EXAMPLES</span></span>

### <span data-ttu-id="09af1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09af1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="09af1-111">Questo comando restituirà l'URL di distribuzione continua del contenitore.</span><span class="sxs-lookup"><span data-stu-id="09af1-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="09af1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09af1-112">PARAMETERS</span></span>

### <span data-ttu-id="09af1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09af1-113">-DefaultProfile</span></span>
<span data-ttu-id="09af1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09af1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09af1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="09af1-115">-Name</span></span>
<span data-ttu-id="09af1-116">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="09af1-116">The name of the web app.</span></span>

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

### <span data-ttu-id="09af1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09af1-117">-ResourceGroupName</span></span>
<span data-ttu-id="09af1-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09af1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="09af1-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="09af1-119">-SlotName</span></span>
<span data-ttu-id="09af1-120">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="09af1-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09af1-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="09af1-121">-WebApp</span></span>
<span data-ttu-id="09af1-122">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="09af1-122">The web app object</span></span>

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

### <span data-ttu-id="09af1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09af1-123">CommonParameters</span></span>
<span data-ttu-id="09af1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09af1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09af1-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09af1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09af1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09af1-126">INPUTS</span></span>

### <span data-ttu-id="09af1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="09af1-127">System.String</span></span>
### <span data-ttu-id="09af1-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="09af1-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="09af1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09af1-129">OUTPUTS</span></span>

### <span data-ttu-id="09af1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09af1-130">System.String</span></span>
## <span data-ttu-id="09af1-131">Note</span><span class="sxs-lookup"><span data-stu-id="09af1-131">NOTES</span></span>

## <span data-ttu-id="09af1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09af1-132">RELATED LINKS</span></span>
