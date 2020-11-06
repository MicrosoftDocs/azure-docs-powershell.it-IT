---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520521"
---
# <span data-ttu-id="34762-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="34762-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="34762-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34762-102">SYNOPSIS</span></span>
<span data-ttu-id="34762-103">Elimina l'emittente di un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="34762-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34762-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34762-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34762-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34762-105">DESCRIPTION</span></span>
<span data-ttu-id="34762-106">Il cmdlet **Remove-AzureKeyVaultCertificateIssuer** Elimina un emittente di certificati da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="34762-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="34762-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34762-107">EXAMPLES</span></span>

### <span data-ttu-id="34762-108">Esempio 1: rimuovere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="34762-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="34762-109">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="34762-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="34762-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34762-110">PARAMETERS</span></span>

### <span data-ttu-id="34762-111">-Force</span><span class="sxs-lookup"><span data-stu-id="34762-111">-Force</span></span>
<span data-ttu-id="34762-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="34762-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34762-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="34762-113">-Name</span></span>
<span data-ttu-id="34762-114">Specifica il nome dell'emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="34762-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34762-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34762-115">-PassThru</span></span>
<span data-ttu-id="34762-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="34762-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34762-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="34762-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34762-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="34762-118">-VaultName</span></span>
<span data-ttu-id="34762-119">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="34762-119">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34762-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34762-120">-Confirm</span></span>
<span data-ttu-id="34762-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34762-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34762-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34762-122">-WhatIf</span></span>
<span data-ttu-id="34762-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34762-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34762-124">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34762-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34762-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34762-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34762-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34762-126">-DefaultProfile</span></span>
<span data-ttu-id="34762-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34762-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34762-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34762-128">CommonParameters</span></span>
<span data-ttu-id="34762-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34762-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34762-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34762-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34762-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34762-131">INPUTS</span></span>

## <span data-ttu-id="34762-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34762-132">OUTPUTS</span></span>

### <span data-ttu-id="34762-133">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="34762-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="34762-134">Note</span><span class="sxs-lookup"><span data-stu-id="34762-134">NOTES</span></span>

## <span data-ttu-id="34762-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34762-135">RELATED LINKS</span></span>

[<span data-ttu-id="34762-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="34762-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="34762-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="34762-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


