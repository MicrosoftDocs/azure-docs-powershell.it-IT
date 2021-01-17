---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327132"
---
# <span data-ttu-id="80de0-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="80de0-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="80de0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80de0-102">SYNOPSIS</span></span>
<span data-ttu-id="80de0-103">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="80de0-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="80de0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80de0-104">SYNTAX</span></span>

### <span data-ttu-id="80de0-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80de0-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80de0-106">S2</span><span class="sxs-lookup"><span data-stu-id="80de0-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80de0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80de0-107">DESCRIPTION</span></span>
<span data-ttu-id="80de0-108">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="80de0-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="80de0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80de0-109">EXAMPLES</span></span>

### <span data-ttu-id="80de0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="80de0-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="80de0-111">Questo comando restituirà l'URL di distribuzione continua del contenitore.</span><span class="sxs-lookup"><span data-stu-id="80de0-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="80de0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80de0-112">PARAMETERS</span></span>

### <span data-ttu-id="80de0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80de0-113">-DefaultProfile</span></span>
<span data-ttu-id="80de0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80de0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80de0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="80de0-115">-Name</span></span>
<span data-ttu-id="80de0-116">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="80de0-116">The name of the web app.</span></span>

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

### <span data-ttu-id="80de0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80de0-117">-ResourceGroupName</span></span>
<span data-ttu-id="80de0-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80de0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="80de0-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="80de0-119">-SlotName</span></span>
<span data-ttu-id="80de0-120">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="80de0-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="80de0-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="80de0-121">-WebApp</span></span>
<span data-ttu-id="80de0-122">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="80de0-122">The web app object</span></span>

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

### <span data-ttu-id="80de0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80de0-123">CommonParameters</span></span>
<span data-ttu-id="80de0-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80de0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80de0-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80de0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80de0-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80de0-126">INPUTS</span></span>

### <span data-ttu-id="80de0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="80de0-127">System.String</span></span>

### <span data-ttu-id="80de0-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="80de0-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="80de0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80de0-129">OUTPUTS</span></span>

### <span data-ttu-id="80de0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="80de0-130">System.String</span></span>

## <span data-ttu-id="80de0-131">Note</span><span class="sxs-lookup"><span data-stu-id="80de0-131">NOTES</span></span>

## <span data-ttu-id="80de0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80de0-132">RELATED LINKS</span></span>
