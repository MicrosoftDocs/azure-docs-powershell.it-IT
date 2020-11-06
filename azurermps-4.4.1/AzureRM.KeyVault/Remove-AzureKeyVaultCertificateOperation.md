---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520520"
---
# <span data-ttu-id="64731-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="64731-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="64731-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64731-102">SYNOPSIS</span></span>
<span data-ttu-id="64731-103">Elimina un'operazione di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="64731-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64731-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64731-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64731-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64731-105">DESCRIPTION</span></span>
<span data-ttu-id="64731-106">Il cmdlet **Remove-AzureKeyVaultCertificateOperation** Elimina un'operazione di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="64731-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="64731-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64731-107">EXAMPLES</span></span>

### <span data-ttu-id="64731-108">Esempio 1: rimuovere un'operazione di certificato</span><span class="sxs-lookup"><span data-stu-id="64731-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="64731-109">Questo comando rimuove l'operazione di certificato denominata TestCert01 dall'archivio della chiave ContosoKV01 senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="64731-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="64731-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64731-110">PARAMETERS</span></span>

### <span data-ttu-id="64731-111">-Force</span><span class="sxs-lookup"><span data-stu-id="64731-111">-Force</span></span>
<span data-ttu-id="64731-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64731-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64731-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="64731-113">-Name</span></span>
<span data-ttu-id="64731-114">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="64731-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64731-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64731-115">-PassThru</span></span>
<span data-ttu-id="64731-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="64731-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="64731-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="64731-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="64731-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="64731-118">-VaultName</span></span>
<span data-ttu-id="64731-119">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="64731-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="64731-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64731-120">-Confirm</span></span>
<span data-ttu-id="64731-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64731-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64731-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64731-122">-WhatIf</span></span>
<span data-ttu-id="64731-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64731-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64731-124">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64731-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64731-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64731-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64731-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64731-126">-DefaultProfile</span></span>
<span data-ttu-id="64731-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64731-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64731-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64731-128">CommonParameters</span></span>
<span data-ttu-id="64731-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64731-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64731-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64731-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64731-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64731-131">INPUTS</span></span>

## <span data-ttu-id="64731-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64731-132">OUTPUTS</span></span>

### <span data-ttu-id="64731-133">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="64731-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="64731-134">Note</span><span class="sxs-lookup"><span data-stu-id="64731-134">NOTES</span></span>

## <span data-ttu-id="64731-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64731-135">RELATED LINKS</span></span>

[<span data-ttu-id="64731-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="64731-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="64731-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="64731-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

