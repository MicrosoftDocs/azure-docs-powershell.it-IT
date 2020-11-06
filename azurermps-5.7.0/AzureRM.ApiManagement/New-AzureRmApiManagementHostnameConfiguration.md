---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508448"
---
# <span data-ttu-id="f36b3-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36b3-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="f36b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f36b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f36b3-103">Crea un'istanza di PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f36b3-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f36b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f36b3-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f36b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f36b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f36b3-106">Il cmdlet **New-AzureRmApiManagementHostnameConfiguration** è un comando helper che crea un'istanza di **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f36b3-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="f36b3-107">Questo comando viene usato con il cmdlet Set-AzureRmApiManagementHostnames.</span><span class="sxs-lookup"><span data-stu-id="f36b3-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="f36b3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f36b3-108">EXAMPLES</span></span>

### <span data-ttu-id="f36b3-109">Esempio 1: creare e inizializzare un'istanza di PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36b3-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="f36b3-110">Questo comando crea e Inizializza un'istanza di **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f36b3-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="f36b3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f36b3-111">PARAMETERS</span></span>

### <span data-ttu-id="f36b3-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f36b3-112">-CertificateThumbprint</span></span>
<span data-ttu-id="f36b3-113">Specifica l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="f36b3-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="f36b3-114">Il certificato deve essere prima importato con il cmdlet Import-AzureRmApiManagementHostnameCertificate.</span><span class="sxs-lookup"><span data-stu-id="f36b3-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

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

### <span data-ttu-id="f36b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36b3-115">-DefaultProfile</span></span>
<span data-ttu-id="f36b3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f36b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f36b3-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="f36b3-117">-Hostname</span></span>
<span data-ttu-id="f36b3-118">Specifica il nome host personalizzato per cui questo cmdlet crea l'istanza di **PsApiManagementHostnameConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f36b3-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

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

### <span data-ttu-id="f36b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36b3-119">CommonParameters</span></span>
<span data-ttu-id="f36b3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f36b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36b3-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f36b3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36b3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f36b3-122">INPUTS</span></span>

### <span data-ttu-id="f36b3-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f36b3-123">None</span></span>
<span data-ttu-id="f36b3-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f36b3-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f36b3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f36b3-125">OUTPUTS</span></span>

### <span data-ttu-id="f36b3-126">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36b3-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="f36b3-127">Note</span><span class="sxs-lookup"><span data-stu-id="f36b3-127">NOTES</span></span>

## <span data-ttu-id="f36b3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f36b3-128">RELATED LINKS</span></span>

[<span data-ttu-id="f36b3-129">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f36b3-129">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="f36b3-130">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f36b3-130">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


