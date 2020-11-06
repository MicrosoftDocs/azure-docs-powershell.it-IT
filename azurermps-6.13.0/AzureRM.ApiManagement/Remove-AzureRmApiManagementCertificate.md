---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a70e3323bbd154005f014f1064a535f45a102f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507751"
---
# <span data-ttu-id="8b541-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8b541-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="8b541-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b541-102">SYNOPSIS</span></span>
<span data-ttu-id="8b541-103">Rimuove un certificato di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8b541-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b541-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b541-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b541-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b541-105">DESCRIPTION</span></span>
<span data-ttu-id="8b541-106">Il cmdlet **Remove-AzureRmApiManagementCertificate** rimuove un certificato di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="8b541-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="8b541-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b541-107">EXAMPLES</span></span>

### <span data-ttu-id="8b541-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="8b541-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="8b541-109">Questo comando rimuove il certificato di gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="8b541-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="8b541-110">Dato che il parametro *Force* è specificato, non è richiesta alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="8b541-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="8b541-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b541-111">PARAMETERS</span></span>

### <span data-ttu-id="8b541-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="8b541-112">-CertificateId</span></span>
<span data-ttu-id="8b541-113">Specifica l'ID del certificato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8b541-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="8b541-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8b541-114">-Context</span></span>
<span data-ttu-id="8b541-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8b541-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b541-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b541-116">-DefaultProfile</span></span>
<span data-ttu-id="8b541-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b541-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b541-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b541-118">-PassThru</span></span>
<span data-ttu-id="8b541-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="8b541-119">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b541-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b541-120">-Confirm</span></span>
<span data-ttu-id="8b541-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b541-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b541-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b541-122">-WhatIf</span></span>
<span data-ttu-id="8b541-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b541-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b541-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b541-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b541-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b541-125">CommonParameters</span></span>
<span data-ttu-id="8b541-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b541-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b541-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b541-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b541-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b541-128">INPUTS</span></span>

### <span data-ttu-id="8b541-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8b541-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b541-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8b541-130">System.String</span></span>

### <span data-ttu-id="8b541-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b541-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b541-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b541-132">OUTPUTS</span></span>

### <span data-ttu-id="8b541-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b541-133">System.Boolean</span></span>

## <span data-ttu-id="8b541-134">Note</span><span class="sxs-lookup"><span data-stu-id="8b541-134">NOTES</span></span>

## <span data-ttu-id="8b541-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b541-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b541-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8b541-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8b541-137">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8b541-137">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8b541-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8b541-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


