---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029891"
---
# <span data-ttu-id="6e350-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="6e350-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="6e350-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e350-102">SYNOPSIS</span></span>
<span data-ttu-id="6e350-103">Configura un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e350-103">Configures an application gateway.</span></span>

## <span data-ttu-id="6e350-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e350-104">SYNTAX</span></span>

### <span data-ttu-id="6e350-105">configFile</span><span class="sxs-lookup"><span data-stu-id="6e350-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e350-106">configObject</span><span class="sxs-lookup"><span data-stu-id="6e350-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e350-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e350-107">DESCRIPTION</span></span>
<span data-ttu-id="6e350-108">Il cmdlet **set-AzureApplicationGatewayConfig** configura un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e350-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="6e350-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e350-109">EXAMPLES</span></span>

### <span data-ttu-id="6e350-110">Esempio 1: configurare un gateway dell'applicazione usando un oggetto Configuration</span><span class="sxs-lookup"><span data-stu-id="6e350-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="6e350-111">Il primo comando ottiene l'oggetto Configuration per il gateway dell'applicazione denominato ApplicationGateway02 usando il cmdlet **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="6e350-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="6e350-112">Il comando lo archivia nella variabile $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="6e350-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="6e350-113">Il secondo comando imposta la configurazione per l'applicazione denominata ApplicationGateway06 tramite un oggetto di configurazione gateway applicazione archiviato nella variabile $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="6e350-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="6e350-114">Esempio 2: configurare un gateway dell'applicazione usando un file di configurazione</span><span class="sxs-lookup"><span data-stu-id="6e350-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="6e350-115">Questo comando imposta la configurazione per l'applicazione denominata ApplicationGateway06 usando un file di configurazione del gateway applicazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="6e350-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="6e350-116">Esempio 3: modificare una configurazione usando un oggetto Configuration</span><span class="sxs-lookup"><span data-stu-id="6e350-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="6e350-117">Il primo comando ottiene l'oggetto Configuration per il gateway dell'applicazione denominato ApplicationGateway06 usando il cmdlet **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="6e350-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="6e350-118">Il comando lo archivia nella variabile $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="6e350-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="6e350-119">Il secondo comando assegna un valore di porta a una proprietà della **porta** nell'oggetto archiviato in $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="6e350-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="6e350-120">Il comando finale passa la $ConfigReturnObject aggiornata al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="6e350-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="6e350-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e350-121">PARAMETERS</span></span>

### <span data-ttu-id="6e350-122">-Config</span><span class="sxs-lookup"><span data-stu-id="6e350-122">-Config</span></span>
<span data-ttu-id="6e350-123">Specifica un oggetto di configurazione gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e350-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="6e350-124">Questo cmdlet assegna la configurazione specificata da questo parametro a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e350-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e350-125">-ConfigFile</span><span class="sxs-lookup"><span data-stu-id="6e350-125">-ConfigFile</span></span>
<span data-ttu-id="6e350-126">Specifica il percorso di un file di configurazione, in formato XML, per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e350-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="6e350-127">Questo cmdlet assegna la configurazione specificata da questo parametro a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e350-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e350-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e350-128">-Name</span></span>
<span data-ttu-id="6e350-129">Specifica il nome del gateway dell'applicazione configurato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e350-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e350-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="6e350-130">-Profile</span></span>
<span data-ttu-id="6e350-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e350-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6e350-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6e350-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e350-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e350-133">CommonParameters</span></span>
<span data-ttu-id="6e350-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e350-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e350-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e350-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e350-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e350-136">INPUTS</span></span>

### <span data-ttu-id="6e350-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e350-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="6e350-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e350-138">OUTPUTS</span></span>

### <span data-ttu-id="6e350-139">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6e350-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="6e350-140">Note</span><span class="sxs-lookup"><span data-stu-id="6e350-140">NOTES</span></span>

## <span data-ttu-id="6e350-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e350-141">RELATED LINKS</span></span>

[<span data-ttu-id="6e350-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="6e350-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


