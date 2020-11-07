---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861269"
---
# <span data-ttu-id="d06e5-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d06e5-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d06e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d06e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d06e5-103">Elimina l'emittente di un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d06e5-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="d06e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d06e5-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d06e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d06e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d06e5-106">Il cmdlet **Remove-AzKeyVaultCertificateIssuer** Elimina un emittente di certificati da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d06e5-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="d06e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d06e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d06e5-108">Esempio 1: rimuovere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="d06e5-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="d06e5-109">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d06e5-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d06e5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d06e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d06e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06e5-111">-DefaultProfile</span></span>
<span data-ttu-id="d06e5-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d06e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d06e5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d06e5-113">-Force</span></span>
<span data-ttu-id="d06e5-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d06e5-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d06e5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d06e5-115">-Name</span></span>
<span data-ttu-id="d06e5-116">Specifica il nome dell'emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d06e5-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06e5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d06e5-117">-PassThru</span></span>
<span data-ttu-id="d06e5-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d06e5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d06e5-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d06e5-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d06e5-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="d06e5-120">-VaultName</span></span>
<span data-ttu-id="d06e5-121">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d06e5-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06e5-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d06e5-122">-Confirm</span></span>
<span data-ttu-id="d06e5-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d06e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06e5-124">-WhatIf</span></span>
<span data-ttu-id="d06e5-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d06e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d06e5-126">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d06e5-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d06e5-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d06e5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06e5-128">CommonParameters</span></span>
<span data-ttu-id="d06e5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06e5-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06e5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06e5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d06e5-131">INPUTS</span></span>

### <span data-ttu-id="d06e5-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d06e5-132">None</span></span>
<span data-ttu-id="d06e5-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d06e5-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d06e5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d06e5-134">OUTPUTS</span></span>

### <span data-ttu-id="d06e5-135">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d06e5-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d06e5-136">Note</span><span class="sxs-lookup"><span data-stu-id="d06e5-136">NOTES</span></span>

## <span data-ttu-id="d06e5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d06e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="d06e5-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d06e5-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d06e5-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d06e5-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


