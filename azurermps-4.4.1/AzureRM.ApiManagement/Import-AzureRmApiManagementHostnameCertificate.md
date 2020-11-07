---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 5d931551491a0df67252f90f6052fdebde15492b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686240"
---
# <span data-ttu-id="ad75c-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ad75c-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="ad75c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad75c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad75c-103">Importa un certificato in un formato PFX per un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ad75c-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad75c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad75c-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad75c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad75c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad75c-106">Il cmdlet **Import-AzureRmApiManagementHostnameCertificate** importa un certificato in un formato pfx per un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ad75c-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="ad75c-107">Il certificato deve essere usato per la configurazione personalizzata dei nomi host.</span><span class="sxs-lookup"><span data-stu-id="ad75c-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="ad75c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad75c-108">EXAMPLES</span></span>

### <span data-ttu-id="ad75c-109">Esempio 1: importare un certificato di gestione API di un nome host</span><span class="sxs-lookup"><span data-stu-id="ad75c-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="ad75c-110">Questo comando importa un certificato per un nome host personalizzato del proxy.</span><span class="sxs-lookup"><span data-stu-id="ad75c-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="ad75c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad75c-111">PARAMETERS</span></span>

### <span data-ttu-id="ad75c-112">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="ad75c-112">-HostnameType</span></span>
<span data-ttu-id="ad75c-113">Specifica il tipo di nome host per cui questo cmdlet carica il certificato.</span><span class="sxs-lookup"><span data-stu-id="ad75c-113">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="ad75c-114">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ad75c-114">Valid values are:</span></span> 

- <span data-ttu-id="ad75c-115">Proxy</span><span class="sxs-lookup"><span data-stu-id="ad75c-115">Proxy</span></span>
- <span data-ttu-id="ad75c-116">Portale</span><span class="sxs-lookup"><span data-stu-id="ad75c-116">Portal</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad75c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad75c-117">-Name</span></span>
<span data-ttu-id="ad75c-118">Specifica il nome della distribuzione di gestione delle API importata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad75c-118">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad75c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad75c-119">-PassThru</span></span>
<span data-ttu-id="ad75c-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ad75c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad75c-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ad75c-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad75c-122">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="ad75c-122">-PfxPassword</span></span>
<span data-ttu-id="ad75c-123">Specifica la password per il file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="ad75c-123">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad75c-124">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="ad75c-124">-PfxPath</span></span>
<span data-ttu-id="ad75c-125">Specifica il percorso di un file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="ad75c-125">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad75c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad75c-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad75c-127">Specifica il nome del gruppo di risorse in cui è presente la distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ad75c-127">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad75c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad75c-128">-DefaultProfile</span></span>
<span data-ttu-id="ad75c-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad75c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad75c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad75c-130">CommonParameters</span></span>
<span data-ttu-id="ad75c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad75c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad75c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad75c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad75c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad75c-133">INPUTS</span></span>

## <span data-ttu-id="ad75c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad75c-134">OUTPUTS</span></span>

### <span data-ttu-id="ad75c-135">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ad75c-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="ad75c-136">Note</span><span class="sxs-lookup"><span data-stu-id="ad75c-136">NOTES</span></span>

## <span data-ttu-id="ad75c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad75c-137">RELATED LINKS</span></span>

[<span data-ttu-id="ad75c-138">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad75c-138">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="ad75c-139">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ad75c-139">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


