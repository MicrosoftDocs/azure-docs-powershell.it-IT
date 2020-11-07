---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: b6825d23244664b475dbd28472dc30f33117a59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686749"
---
# <span data-ttu-id="97561-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="97561-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="97561-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97561-102">SYNOPSIS</span></span>
<span data-ttu-id="97561-103">Ottiene i certificati di gestione delle API configurati per l'autenticazione reciproca con backend nel servizio.</span><span class="sxs-lookup"><span data-stu-id="97561-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97561-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97561-104">SYNTAX</span></span>

### <span data-ttu-id="97561-105">GetAllCertificates (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97561-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97561-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="97561-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97561-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97561-107">DESCRIPTION</span></span>
<span data-ttu-id="97561-108">Il cmdlet **Get-AzureRmApiManagementCertificate** ottiene tutti i certificati o i certificati di gestione delle API di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="97561-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="97561-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97561-109">EXAMPLES</span></span>

### <span data-ttu-id="97561-110">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="97561-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="97561-111">Questo comando ottiene tutti i certificati di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="97561-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="97561-112">Esempio 2: ottenere un certificato in base all'ID</span><span class="sxs-lookup"><span data-stu-id="97561-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="97561-113">Questo comando ottiene il certificato di gestione delle API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="97561-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="97561-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97561-114">PARAMETERS</span></span>

### <span data-ttu-id="97561-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="97561-115">-CertificateId</span></span>
<span data-ttu-id="97561-116">Specifica l'ID del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="97561-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByCertificateId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97561-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="97561-117">-Context</span></span>
<span data-ttu-id="97561-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="97561-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97561-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97561-119">-DefaultProfile</span></span>
<span data-ttu-id="97561-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97561-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="97561-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97561-121">-Confirm</span></span>
<span data-ttu-id="97561-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97561-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97561-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97561-123">-WhatIf</span></span>
<span data-ttu-id="97561-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97561-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97561-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97561-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97561-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97561-126">CommonParameters</span></span>
<span data-ttu-id="97561-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97561-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97561-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97561-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97561-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97561-129">INPUTS</span></span>

### <span data-ttu-id="97561-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97561-130">None</span></span>
<span data-ttu-id="97561-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="97561-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97561-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97561-132">OUTPUTS</span></span>

### <span data-ttu-id="97561-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="97561-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="97561-134">Note</span><span class="sxs-lookup"><span data-stu-id="97561-134">NOTES</span></span>

## <span data-ttu-id="97561-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97561-135">RELATED LINKS</span></span>

[<span data-ttu-id="97561-136">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="97561-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="97561-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="97561-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="97561-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="97561-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


