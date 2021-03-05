---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 8e4ed309d4109ecfe230a522a65054213ae32049
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972334"
---
# <span data-ttu-id="a7c8d-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a7c8d-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="a7c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c8d-103">Crea un certificato gestito del servizio app per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="a7c8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7c8d-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7c8d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c8d-106">Il cmdlet **New-AzWebAppCertificate** crea un certificato gestito del servizio app di Azure</span><span class="sxs-lookup"><span data-stu-id="a7c8d-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="a7c8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7c8d-107">EXAMPLES</span></span>

### <span data-ttu-id="a7c8d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7c8d-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="a7c8d-109">Questo comando crea un certificato gestito dal servizio app per la WebApp specificata</span><span class="sxs-lookup"><span data-stu-id="a7c8d-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="a7c8d-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a7c8d-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="a7c8d-111">Questo comando crea un certificato gestito dal servizio app e viene associato al dato slot WebApp.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="a7c8d-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a7c8d-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="a7c8d-113">Questo comando crea un certificato gestito dal servizio app e viene associato alla WebApp specificata.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="a7c8d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7c8d-114">PARAMETERS</span></span>

### <span data-ttu-id="a7c8d-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="a7c8d-115">-AddBinding</span></span>
<span data-ttu-id="a7c8d-116">Per aggiungere il certificato creato alla WebApp/slot.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c8d-117">-DefaultProfile</span></span>
<span data-ttu-id="a7c8d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c8d-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="a7c8d-119">-HostName</span></span>
<span data-ttu-id="a7c8d-120">Nomi host personalizzati associati all'app/slot Web.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c8d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a7c8d-121">-Name</span></span>
<span data-ttu-id="a7c8d-122">Nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c8d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c8d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7c8d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7c8d-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="a7c8d-125">-Slot</span></span>
<span data-ttu-id="a7c8d-126">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-126">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a7c8d-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="a7c8d-127">-SslState</span></span>
<span data-ttu-id="a7c8d-128">Opzione stato SSL.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-128">Ssl state option.</span></span>
<span data-ttu-id="a7c8d-129">Usare "SniEnabled" o "IpBasedEnabled".</span><span class="sxs-lookup"><span data-stu-id="a7c8d-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="a7c8d-130">L'opzione predefinita è "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="a7c8d-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c8d-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a7c8d-131">-WebAppName</span></span>
<span data-ttu-id="a7c8d-132">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c8d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c8d-133">CommonParameters</span></span>
<span data-ttu-id="a7c8d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c8d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7c8d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c8d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7c8d-136">INPUTS</span></span>

### <span data-ttu-id="a7c8d-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7c8d-137">None</span></span>

## <span data-ttu-id="a7c8d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7c8d-138">OUTPUTS</span></span>

### <span data-ttu-id="a7c8d-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="a7c8d-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="a7c8d-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7c8d-140">NOTES</span></span>

## <span data-ttu-id="a7c8d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7c8d-141">RELATED LINKS</span></span>
[<span data-ttu-id="a7c8d-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a7c8d-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)