---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023623"
---
# <span data-ttu-id="b1b74-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="b1b74-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="b1b74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1b74-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b74-103">Ottiene un contesto di configurazione del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1b74-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="b1b74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1b74-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1b74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1b74-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b74-106">Il cmdlet **Get-AzureApplicationGatewayConfig** ottiene un contesto di configurazione di Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b1b74-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="b1b74-107">Un contesto include sia un oggetto Configuration che una configurazione XML.</span><span class="sxs-lookup"><span data-stu-id="b1b74-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="b1b74-108">È possibile salvare la configurazione XML in un file.</span><span class="sxs-lookup"><span data-stu-id="b1b74-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="b1b74-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1b74-109">EXAMPLES</span></span>

### <span data-ttu-id="b1b74-110">Esempio 1: ottenere una configurazione del gateway dell'applicazione e salvarla in un file</span><span class="sxs-lookup"><span data-stu-id="b1b74-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="b1b74-111">Questo comando consente di ottenere la configurazione di un gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="b1b74-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="b1b74-112">Il comando lo salva nel file nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b1b74-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="b1b74-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1b74-113">PARAMETERS</span></span>

### <span data-ttu-id="b1b74-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="b1b74-114">-ExportToFile</span></span>
<span data-ttu-id="b1b74-115">Specifica un percorso di file a cui questo cmdlet salva la configurazione in formato XML.</span><span class="sxs-lookup"><span data-stu-id="b1b74-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b74-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1b74-116">-Name</span></span>
<span data-ttu-id="b1b74-117">Specifica il nome del gateway dell'applicazione per cui questo cmdlet ottiene le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b1b74-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b74-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1b74-118">-Profile</span></span>
<span data-ttu-id="b1b74-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b74-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b1b74-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b1b74-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1b74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b74-121">CommonParameters</span></span>
<span data-ttu-id="b1b74-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b74-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b74-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b74-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1b74-124">INPUTS</span></span>

### <span data-ttu-id="b1b74-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b1b74-125">System.String</span></span>

## <span data-ttu-id="b1b74-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1b74-126">OUTPUTS</span></span>

### <span data-ttu-id="b1b74-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="b1b74-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="b1b74-128">Note</span><span class="sxs-lookup"><span data-stu-id="b1b74-128">NOTES</span></span>

## <span data-ttu-id="b1b74-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1b74-129">RELATED LINKS</span></span>

[<span data-ttu-id="b1b74-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="b1b74-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


