---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: ed7ad2edb0c82203f571edccf9b6672428956ac2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676318"
---
# <span data-ttu-id="d22f7-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="d22f7-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="d22f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d22f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f7-103">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="d22f7-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="d22f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d22f7-104">SYNTAX</span></span>

### <span data-ttu-id="d22f7-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d22f7-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d22f7-106">S2</span><span class="sxs-lookup"><span data-stu-id="d22f7-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d22f7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d22f7-107">DESCRIPTION</span></span>
<span data-ttu-id="d22f7-108">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="d22f7-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="d22f7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d22f7-109">EXAMPLES</span></span>

### <span data-ttu-id="d22f7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d22f7-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="d22f7-111">Questo comando restituirà l'URL di distribuzione continua del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d22f7-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="d22f7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d22f7-112">PARAMETERS</span></span>

### <span data-ttu-id="d22f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22f7-113">-DefaultProfile</span></span>
<span data-ttu-id="d22f7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d22f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22f7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d22f7-115">-Name</span></span>
<span data-ttu-id="d22f7-116">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="d22f7-116">The name of the web app.</span></span>

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

### <span data-ttu-id="d22f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d22f7-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d22f7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d22f7-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="d22f7-119">-SlotName</span></span>
<span data-ttu-id="d22f7-120">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="d22f7-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="d22f7-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="d22f7-121">-WebApp</span></span>
<span data-ttu-id="d22f7-122">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="d22f7-122">The web app object</span></span>

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

### <span data-ttu-id="d22f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f7-123">CommonParameters</span></span>
<span data-ttu-id="d22f7-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f7-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22f7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f7-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d22f7-126">INPUTS</span></span>

### <span data-ttu-id="d22f7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d22f7-127">System.String</span></span>

### <span data-ttu-id="d22f7-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d22f7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d22f7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d22f7-129">OUTPUTS</span></span>

### <span data-ttu-id="d22f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d22f7-130">System.String</span></span>

## <span data-ttu-id="d22f7-131">Note</span><span class="sxs-lookup"><span data-stu-id="d22f7-131">NOTES</span></span>

## <span data-ttu-id="d22f7-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d22f7-132">RELATED LINKS</span></span>
