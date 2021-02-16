---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207490"
---
# <span data-ttu-id="1dcb0-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1dcb0-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="1dcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcb0-103">Ottiene un binding SSL del certificato Web App di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="1dcb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dcb0-104">SYNTAX</span></span>

### <span data-ttu-id="1dcb0-105">S1</span><span class="sxs-lookup"><span data-stu-id="1dcb0-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dcb0-106">S2</span><span class="sxs-lookup"><span data-stu-id="1dcb0-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dcb0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dcb0-107">DESCRIPTION</span></span>
<span data-ttu-id="1dcb0-108">Il cmdlet **Get-AzWebAppSSLBinding** ottiene un binding SSL (Secure Sockets Layer) per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="1dcb0-109">Le associazioni SSL vengono usate per associare un'app Web a un certificato caricato.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="1dcb0-110">Le app Web possono essere associate a più certificati.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="1dcb0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dcb0-111">EXAMPLES</span></span>

### <span data-ttu-id="1dcb0-112">Esempio 1: Ottenere i binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="1dcb0-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="1dcb0-113">Questo comando recupera le associazioni SSL per l'app Web ContosoWebApp, associata al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="1dcb0-114">Esempio 2: Usare un riferimento a un oggetto per ottenere i binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="1dcb0-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="1dcb0-115">I comandi di questo esempio ottengono anche i binding SSL per l'app Web ContosoWebApp; In questo caso, invece del nome dell'app Web e del gruppo di risorse associato, viene usato un riferimento a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="1dcb0-116">Questo riferimento all'oggetto viene creato dal primo comando dell'esempio, che usa **Get-AzWebApp** per creare un riferimento a un oggetto all'app Web denominato ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="1dcb0-117">Il riferimento all'oggetto viene archiviato in una variabile denominata $WebApp.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="1dcb0-118">Questa variabile e il cmdlet **Get-AzWebAppSSLBinding** vengono quindi usati dal secondo comando per ottenere le associazioni SSL.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="1dcb0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dcb0-119">PARAMETERS</span></span>

### <span data-ttu-id="1dcb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcb0-120">-DefaultProfile</span></span>
<span data-ttu-id="1dcb0-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dcb0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1dcb0-122">-Name</span></span>
<span data-ttu-id="1dcb0-123">Specifica il nome del binding SSL.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dcb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dcb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dcb0-125">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="1dcb0-126">Non è possibile usare *il parametro ResourceGroupName* e il *parametro WebApp* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="1dcb0-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="1dcb0-127">-Slot</span></span>
<span data-ttu-id="1dcb0-128">Specifica uno slot di distribuzione di Web App.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="1dcb0-129">Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzWebAppSlot distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dcb0-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1dcb0-130">-WebApp</span></span>
<span data-ttu-id="1dcb0-131">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-131">Specifies a Web App.</span></span>
<span data-ttu-id="1dcb0-132">Per ottenere un'app Web, usare il cmdlet Get-AzWebApp web app.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="1dcb0-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="1dcb0-133">-WebAppName</span></span>
<span data-ttu-id="1dcb0-134">Specifica il nome dell'app Web da cui il cmdlet ottiene le associazioni SSL.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="1dcb0-135">Non è possibile usare *il parametro WebAppName* e il *parametro WebApp* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dcb0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcb0-136">CommonParameters</span></span>
<span data-ttu-id="1dcb0-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dcb0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcb0-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dcb0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcb0-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dcb0-139">INPUTS</span></span>

### <span data-ttu-id="1dcb0-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1dcb0-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1dcb0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dcb0-141">OUTPUTS</span></span>

### <span data-ttu-id="1dcb0-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="1dcb0-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="1dcb0-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dcb0-143">NOTES</span></span>

## <span data-ttu-id="1dcb0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dcb0-144">RELATED LINKS</span></span>

[<span data-ttu-id="1dcb0-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1dcb0-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="1dcb0-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1dcb0-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="1dcb0-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1dcb0-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


