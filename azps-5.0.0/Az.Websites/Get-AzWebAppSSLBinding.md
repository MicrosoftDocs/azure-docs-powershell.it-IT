---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302310"
---
# <span data-ttu-id="07d44-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="07d44-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="07d44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07d44-102">SYNOPSIS</span></span>
<span data-ttu-id="07d44-103">Ottiene un binding SSL certificato di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="07d44-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="07d44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07d44-104">SYNTAX</span></span>

### <span data-ttu-id="07d44-105">S1</span><span class="sxs-lookup"><span data-stu-id="07d44-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d44-106">S2</span><span class="sxs-lookup"><span data-stu-id="07d44-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07d44-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d44-107">DESCRIPTION</span></span>
<span data-ttu-id="07d44-108">Il cmdlet **Get-AzWebAppSSLBinding** ottiene un binding SSL (Secure Sockets Layer) per una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="07d44-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="07d44-109">I binding SSL vengono usati per associare un'app Web a un certificato caricato.</span><span class="sxs-lookup"><span data-stu-id="07d44-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="07d44-110">Le app Web possono essere associate a più certificati.</span><span class="sxs-lookup"><span data-stu-id="07d44-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="07d44-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07d44-111">EXAMPLES</span></span>

### <span data-ttu-id="07d44-112">Esempio 1: ottenere binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="07d44-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="07d44-113">Questo comando recupera i binding SSL per l'app Web ContosoWebApp, associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="07d44-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="07d44-114">Esempio 2: usare un riferimento a un oggetto per ottenere binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="07d44-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="07d44-115">I comandi in questo esempio ottengono anche i binding SSL per l'app Web ContosoWebApp; in questo caso, tuttavia, viene usato un riferimento a un oggetto al posto del nome dell'app Web e del nome del gruppo di risorse associato.</span><span class="sxs-lookup"><span data-stu-id="07d44-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="07d44-116">Questo riferimento all'oggetto viene creato dal primo comando dell'esempio, che usa **Get-AzWebApp** per creare un riferimento a un oggetto all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="07d44-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="07d44-117">Il riferimento a un oggetto viene archiviato in una variabile denominata $WebApp.</span><span class="sxs-lookup"><span data-stu-id="07d44-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="07d44-118">Questa variabile e il cmdlet **Get-AzWebAppSSLBinding** vengono quindi usati dal secondo comando per ottenere i binding SSL.</span><span class="sxs-lookup"><span data-stu-id="07d44-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="07d44-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07d44-119">PARAMETERS</span></span>

### <span data-ttu-id="07d44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d44-120">-DefaultProfile</span></span>
<span data-ttu-id="07d44-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07d44-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d44-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="07d44-122">-Name</span></span>
<span data-ttu-id="07d44-123">Specifica il nome del binding SSL.</span><span class="sxs-lookup"><span data-stu-id="07d44-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="07d44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d44-124">-ResourceGroupName</span></span>
<span data-ttu-id="07d44-125">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="07d44-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="07d44-126">Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="07d44-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="07d44-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="07d44-127">-Slot</span></span>
<span data-ttu-id="07d44-128">Specifica uno slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="07d44-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="07d44-129">Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="07d44-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="07d44-130">-Web App</span><span class="sxs-lookup"><span data-stu-id="07d44-130">-WebApp</span></span>
<span data-ttu-id="07d44-131">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="07d44-131">Specifies a Web App.</span></span>
<span data-ttu-id="07d44-132">Per ottenere un'app Web, usa il cmdlet Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="07d44-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="07d44-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="07d44-133">-WebAppName</span></span>
<span data-ttu-id="07d44-134">Specifica il nome dell'app Web da cui questo cmdlet ottiene i binding SSL.</span><span class="sxs-lookup"><span data-stu-id="07d44-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="07d44-135">Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="07d44-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="07d44-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d44-136">CommonParameters</span></span>
<span data-ttu-id="07d44-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d44-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d44-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d44-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d44-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07d44-139">INPUTS</span></span>

### <span data-ttu-id="07d44-140">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="07d44-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="07d44-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07d44-141">OUTPUTS</span></span>

### <span data-ttu-id="07d44-142">Microsoft. Azure. Management. website. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="07d44-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="07d44-143">Note</span><span class="sxs-lookup"><span data-stu-id="07d44-143">NOTES</span></span>

## <span data-ttu-id="07d44-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07d44-144">RELATED LINKS</span></span>

[<span data-ttu-id="07d44-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="07d44-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="07d44-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="07d44-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="07d44-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="07d44-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


