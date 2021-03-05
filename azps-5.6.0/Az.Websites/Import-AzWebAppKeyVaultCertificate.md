---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007421"
---
# <span data-ttu-id="2f11f-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2f11f-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="2f11f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f11f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f11f-103">Importare un certificato SSL in un'app Web dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="2f11f-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="2f11f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f11f-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f11f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2f11f-105">DESCRIPTION</span></span>
<span data-ttu-id="2f11f-106">Il cmdlet **Import-AzWebAppKeyVaultCertificate** importa un certificato SSL in un'app Web dal Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="2f11f-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="2f11f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f11f-107">EXAMPLES</span></span>

### <span data-ttu-id="2f11f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2f11f-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="2f11f-109">Questo comando importa un certificato SSL in un'app Web dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="2f11f-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="2f11f-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2f11f-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="2f11f-111">Questo comando importa un certificato SSL in un'app Web dal Vault delle chiavi usando l'ID risorsa (in genere se il Vault chiave si trova in un altro abbonamento).</span><span class="sxs-lookup"><span data-stu-id="2f11f-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="2f11f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f11f-112">PARAMETERS</span></span>

### <span data-ttu-id="2f11f-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="2f11f-113">-CertName</span></span>
<span data-ttu-id="2f11f-114">KeyVaultCertName del certificato creato in keyvault</span><span class="sxs-lookup"><span data-stu-id="2f11f-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f11f-115">-DefaultProfile</span></span>
<span data-ttu-id="2f11f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f11f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f11f-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="2f11f-117">-KeyVaultName</span></span>
<span data-ttu-id="2f11f-118">Nome della chiavevaultato.</span><span class="sxs-lookup"><span data-stu-id="2f11f-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f11f-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f11f-120">Nome del gruppo di risorse dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="2f11f-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="2f11f-121">-Slot</span></span>
<span data-ttu-id="2f11f-122">Nome dello slot della WebApp.</span><span class="sxs-lookup"><span data-stu-id="2f11f-122">The name of the webapp slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2f11f-123">-WebAppName</span></span>
<span data-ttu-id="2f11f-124">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="2f11f-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f11f-125">-Confirm</span></span>
<span data-ttu-id="2f11f-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f11f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f11f-127">-WhatIf</span></span>
<span data-ttu-id="2f11f-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f11f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f11f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f11f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f11f-130">CommonParameters</span></span>
<span data-ttu-id="2f11f-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f11f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f11f-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f11f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f11f-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="2f11f-133">INPUTS</span></span>

### <span data-ttu-id="2f11f-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2f11f-134">None</span></span>

## <span data-ttu-id="2f11f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f11f-135">OUTPUTS</span></span>

### <span data-ttu-id="2f11f-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="2f11f-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="2f11f-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="2f11f-137">NOTES</span></span>

## <span data-ttu-id="2f11f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f11f-138">RELATED LINKS</span></span>
