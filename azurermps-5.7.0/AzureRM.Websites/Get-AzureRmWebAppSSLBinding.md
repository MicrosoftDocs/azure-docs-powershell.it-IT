---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: c2780b05e6caae6e200e7fbab26f02a6644f9ebc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509516"
---
# <span data-ttu-id="89399-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="89399-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="89399-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89399-102">SYNOPSIS</span></span>
<span data-ttu-id="89399-103">Ottiene un binding SSL certificato di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="89399-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89399-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89399-104">SYNTAX</span></span>

### <span data-ttu-id="89399-105">S1</span><span class="sxs-lookup"><span data-stu-id="89399-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89399-106">S2</span><span class="sxs-lookup"><span data-stu-id="89399-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89399-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89399-107">DESCRIPTION</span></span>
<span data-ttu-id="89399-108">Il cmdlet **Get-AzureRmWebAppSSLBinding** ottiene un binding SSL (Secure Sockets Layer) per una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="89399-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="89399-109">I binding SSL vengono usati per associare un'app Web a un certificato caricato.</span><span class="sxs-lookup"><span data-stu-id="89399-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="89399-110">Le app Web possono essere associate a più certificati.</span><span class="sxs-lookup"><span data-stu-id="89399-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="89399-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89399-111">EXAMPLES</span></span>

### <span data-ttu-id="89399-112">Esempio 1: ottenere binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="89399-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="89399-113">Questo comando recupera i binding SSL per l'app Web ContosoWebApp, associato al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="89399-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="89399-114">Esempio 2: usare un riferimento a un oggetto per ottenere binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="89399-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="89399-115">I comandi in questo esempio ottengono anche i binding SSL per l'app Web ContosoWebApp; in questo caso, tuttavia, viene usato un riferimento a un oggetto al posto del nome dell'app Web e del nome del gruppo di risorse associato.</span><span class="sxs-lookup"><span data-stu-id="89399-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="89399-116">Questo riferimento all'oggetto viene creato dal primo comando dell'esempio, che usa **Get-AzureRmWebApp** per creare un riferimento a un oggetto all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="89399-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="89399-117">Il riferimento a un oggetto viene archiviato in una variabile denominata $WebApp.</span><span class="sxs-lookup"><span data-stu-id="89399-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="89399-118">Questa variabile e il cmdlet **Get-AzureRmWebAppSSLBinding** vengono quindi usati dal secondo comando per ottenere i binding SSL.</span><span class="sxs-lookup"><span data-stu-id="89399-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="89399-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89399-119">PARAMETERS</span></span>

### <span data-ttu-id="89399-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89399-120">-DefaultProfile</span></span>
<span data-ttu-id="89399-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89399-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89399-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="89399-122">-Name</span></span>
<span data-ttu-id="89399-123">Specifica il nome del binding SSL.</span><span class="sxs-lookup"><span data-stu-id="89399-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="89399-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89399-124">-ResourceGroupName</span></span>
<span data-ttu-id="89399-125">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="89399-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="89399-126">Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="89399-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="89399-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="89399-127">-Slot</span></span>
<span data-ttu-id="89399-128">Specifica uno slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="89399-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="89399-129">Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="89399-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="89399-130">-Web App</span><span class="sxs-lookup"><span data-stu-id="89399-130">-WebApp</span></span>
<span data-ttu-id="89399-131">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="89399-131">Specifies a Web App.</span></span>
<span data-ttu-id="89399-132">Per ottenere un'app Web, usa il cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="89399-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

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

### <span data-ttu-id="89399-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="89399-133">-WebAppName</span></span>
<span data-ttu-id="89399-134">Specifica il nome dell'app Web da cui questo cmdlet ottiene i binding SSL.</span><span class="sxs-lookup"><span data-stu-id="89399-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="89399-135">Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="89399-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="89399-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89399-136">CommonParameters</span></span>
<span data-ttu-id="89399-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89399-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89399-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89399-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89399-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89399-139">INPUTS</span></span>

### <span data-ttu-id="89399-140">Sito</span><span class="sxs-lookup"><span data-stu-id="89399-140">Site</span></span>
<span data-ttu-id="89399-141">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="89399-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="89399-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89399-142">OUTPUTS</span></span>

## <span data-ttu-id="89399-143">Note</span><span class="sxs-lookup"><span data-stu-id="89399-143">NOTES</span></span>

## <span data-ttu-id="89399-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89399-144">RELATED LINKS</span></span>

[<span data-ttu-id="89399-145">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="89399-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="89399-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="89399-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="89399-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="89399-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


